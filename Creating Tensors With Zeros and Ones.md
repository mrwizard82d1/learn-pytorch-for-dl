In addition to creating random tensors, one often creates tensors consisting of
- All zeros
- All ones
This technique allows one to *mask out* other values

Each tensor has a *datatype*
- The default is `float32`
- But can also be `int64`
- And many others (See [torch.tensor](https://pytorch.org/docs/stable/tensors.html#data-types))

```
all_zeros = torch.zeros(2, 3)
all_ones = torch.ones(5, 7)
```

