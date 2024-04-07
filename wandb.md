# How do I track the experiments done & best results?



## Wandb
One of the best solutions currently used is Wandb, ie Weights & Biases. 

Using it is as simple as just the following

```
# Log in to your W&B account
import wandb
wandb.login()
```

With HuggingFace transformers you can do the following:
```
# Optional: log both gradients and parameters
%env WANDB_WATCH=all
```

Now just run your training script and see how wandb logs all the required data.

## Neptune AI
[]: # TODO: Add here


## References

This project uses code from the following source:
- **Wandb**: Available at: [URL to the original source](https://wandb.ai/)
