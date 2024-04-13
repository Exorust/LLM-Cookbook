# How to load a public dataset for use?

## Basic Premise
HuggingFace already contains high quality datasets that one can use. 

You can load a dataset with the common load_dataset()
```
from datasets import load_dataset

dataset = load_dataset("rotten_tomatoes", split="train")
```

### Splitting the Dataset
Most datasets are already split into `train` and `test` splits. The splits are present on the dataset page. Youcan also list the split names with get_dataset_split_names() function:
```
from datasets import get_dataset_split_names

get_dataset_split_names("rotten_tomatoes")
>>> ['train', 'validation', 'test']
```

Loading a dataset split returns a Dataset object:
```
from datasets import load_dataset

dataset = load_dataset("rotten_tomatoes", split="train")

dataset
>>> Dataset({
    features: ['text', 'label'],
    num_rows: 8530
})
```

If you don’t specify a split, 🤗 Datasets returns a DatasetDict object instead:
```
from datasets import load_dataset

dataset = load_dataset("rotten_tomatoes")
>>> DatasetDict({
    train: Dataset({
        features: ['text', 'label'],
        num_rows: 8530
    })
    validation: Dataset({
        features: ['text', 'label'],
        num_rows: 1066
    })
    test: Dataset({
        features: ['text', 'label'],
        num_rows: 1066
    })
})
```


## See Also
- [Datasets: Load from Hub](https://huggingface.co/docs/datasets/en/load_hub)

## References

This project uses code from the following source:
- **HuggingFace**: Available at: [Datasets: Load from Hub](https://huggingface.co/docs/datasets/en/load_hub)