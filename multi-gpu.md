# How to train an LLM with multiple GPUs?

## Basic Premise
HuggingFace itself provides accelerate which allows one to run Pytorch code on a distributed Configuration. 


You can setup accelerate and the configuration of your GPUs in the command line here:
```
$ accelerate config
```

The next main feature of Accelerate is the Accelerator class which adapts your PyTorch code to run on different distributed setups.

You only need to add a few lines of code to your training script to enable it to run on multiple GPUs or TPUs.
```
+ from accelerate import Accelerator
+ accelerator = Accelerator()

+ device = accelerator.device
+ model, optimizer, training_dataloader, scheduler = accelerator.prepare(
+     model, optimizer, training_dataloader, scheduler
+ )

  for batch in training_dataloader:
      optimizer.zero_grad()
      inputs, targets = batch
-     inputs = inputs.to(device)
-     targets = targets.to(device)
      outputs = model(inputs)
      loss = loss_function(outputs, targets)
+     accelerator.backward(loss)
      optimizer.step()
      scheduler.step()
```
1. Import and instantiate the Accelerator class at the beginning of your training script. The Accelerator class initializes everything necessary for distributed training, and it automatically detects your training environment (a single machine with a GPU, a machine with several GPUs, several machines with multiple GPUs or a TPU, etc.) based on how the code was launched.

```
from accelerate import Accelerator

accelerator = Accelerator()
```
2. Remove calls like .cuda() on your model and input data. The Accelerator class automatically places these objects on the appropriate device for you.
```
device = accelerator.device
```
3. Pass all relevant PyTorch objects for training (optimizer, model, dataloader(s), learning rate scheduler) to the prepare() method as soon as they’re created. This method wraps the model in a container optimized for your distributed setup, uses Accelerates version of the optimizer and scheduler, and creates a sharded version of your dataloader for distribution across GPUs or TPUs.
```
model, optimizer, train_dataloader, lr_scheduler = accelerator.prepare(
    model, optimizer, train_dataloader, lr_scheduler
)
```
4. Replace loss.backward() with backward() to use the correct backward() method for your training setup.
```
accelerator.backward(loss)
```
## Sharding training across multiple GPUs
As long as you have followed the above steps and kept everything in a main() function you can now shard your training across multiple GPUs.


You need to specify your config with `accelerate config` and then, you need to launch it with `accelerate launch`.

## Sharding the model itself across multiple GPUs
To allow this to work we will need to enable `Fully Sharded Data Parallel` which is available in pytorch in `accelerate`.

Setup your FSDP as following:

```
from accelerate import FullyShardedDataParallelPlugin
from torch.distributed.fsdp.fully_sharded_data_parallel import FullOptimStateDictConfig, FullStateDictConfig

fsdp_plugin = FullyShardedDataParallelPlugin(
    state_dict_config=FullStateDictConfig(offload_to_cpu=False, rank0_only=False),
    optim_state_dict_config=FullOptimStateDictConfig(offload_to_cpu=False, rank0_only=False),
)

accelerator = Accelerator(fsdp_plugin=fsdp_plugin)
```

And run with Accelerate.


## See Also
- [HuggingFace: Accelerate](https://huggingface.co/docs/accelerate/index)
- [HuggingFace: Fully Sharded Data Parallel](https://huggingface.co/docs/accelerate/usage_guides/fsdp)


## References

This project uses code from the following source:
- **HuggingFace Accelerate**: Available at: [URL to the original source](https://huggingface.co/docs/accelerate/index)
- **HuggingFace FSDP**: Available at: [URL to the original source]((https://huggingface.co/docs/accelerate/usage_guides/fsdp))