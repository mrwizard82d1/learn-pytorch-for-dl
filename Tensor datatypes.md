Tensors **must** have a datatype; the default type for the constructor `tensor.Tensor` is `torch.float32`

| If the dype is `None` and the initial values | Then the tensor has the dtype      |
| -------------------------------------------- | ---------------------------------- |
| Have at least one `float`                    | `torch.float32` (or `torch.float`) |
| Are all integers                             | `torch.int64` (or `torch.double`)  |
| Are all bool                                 | `torch.bool`                       |
```python
# Float 32 tensor
float_32_tensor = torch.tensor([3.0, 6.0, 9.0])
float_32_tensor, float_32_tensor.dtype

# The previous expression will contain the three values we specificied and the tensor will be of type `torch.float32`
```

Other parameters to `torch.tensor`:

- `device`  (A value of `None` puts the tensor on the CPU)
	- Other valid CPU values are
		- `cpu`
		- `cuda` for NVIDIA GPU's
		- `mpu` for Mac GPU's
- `requires_grad` (A boolean - a value of `False` is the default)

**Note** Tensor datatypes is one of the "big three" errors encountered in PyTorch
- Not right **datatype**
- Not right **shape**
- Not on the right **device**

One can create one tensor from another tensor and change the type of the new tensor

```python
float_16_tensor = float_32_tensor.type(torch.float16)
float_16_tensor, float_16_tensor.dtype

# The `dtype` of `float_16_tensor` is `torch.float16` (or `torch.half`)
```

Exercise: try adding tensors of different types

```python
sum_float32_and_int64 = float_32_tensor + float_64_tensor
sum_float32_and_int64, sum_float32_and_int64.dtype

# Returns type `(tensor([6., 12., 18.], torch.float32)`
```

```python
sum_float32_and_bool = float_32_tensor + bool_tensor
sum_float32_and_bool, sum_float32_and_float64.dtype

# Returns type `(tensor([4., 6., 9.], torch.float32)`
```

```python
sum_float32_and_float64 = float_32_tensor + float_64_tensor
sum_float32_and_float64, sum_float32_and_float64.dtype

# Returns type `(tensor([4., 6., 9.], torch.float64)`
```