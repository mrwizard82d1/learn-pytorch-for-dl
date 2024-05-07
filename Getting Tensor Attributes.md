To get information from a tensor, try:

| If you want to get | Query the property |
| ------------------ | ------------------ |
| datatype           | `tensor.dtype`     |
| shape              | `tensor.shape`     |
| device             | `tensor.device`    |
For example, let's create a tensor.
```python
some_tensor = torch.rand(3, 4)  ## A random tensor with 3 rows and 4 columns
some_tensor
```

Each of the following expressions will return a property of interest:

- `some_tensor.dtype`
- `some_tensor.shape`
- `some_tensor.device`

For example, imagine we entered the following code into a `jupyter` cell:

```python
print(some_tensor)
printf('Datatype of tensor: {some_tensor.dtype}')
printf('Shape of tensor: {some_tensor.shape}')
printf('Device tensor is on: {some_tensor.device}')
```

An alternative to `tensor.shape` is the *function* `tensor.size()`