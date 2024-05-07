# How to create a tensor range

```
# Create a tensor with values in a range
tensor_with_range = torch.arange(1, 11) ## Values from 1 (inclusive) to 10 (exclusive)
```

See[ torch.arange()](https://pytorch.org/docs/stable/tensors.html#data-types)

## Create one tensor like another

```
ten_zeros = torch.zeros_like(input=tensor_with_range)
ten_ones = torch.ones_like(input=tensor_with_range)
```

