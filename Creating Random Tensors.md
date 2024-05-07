### Random tensors

Why random tensors?
- Many neural networks start as **random tensors** and then adjust these numbers to better represent the data.
- Basic algorithm
	- Start with random numbers
	- Learn from data
	- Update random numbers
	- Repeat until good enough

```code

# Create a random tensor of size (3, 4)
random_tensor = torch.rand(3, 4)
```

Number of dimensions is 3x4 (a matrix).

In image projects, data is often of size 224x224x3
- 224 pixels (horizontal x vertical)
- 3 colors (RGB)
- Typical representation for images is height x width x colors

