- Definition
	- Finding the `min`, `max`, `mean`, `sum`, etc
- Call
	- If `tensor = torch.arange(0, 100, 10)`
	- `torch.min(tensor)` or `tensor.min()
	- `torch.max(tensor)` or `tensor.min()`
	- `torch.mean(tensor)` or `tensor.mean()`
	- `torch.sum(tensor)` or `tensor.sum()`
- Calling `torch.mean()` fails in this scenario
	- Because `torch.mean()` expects a tensor of type `torch.float32`
		- At least at the time of the video
	- Note that `torch.arange()` **did not** specify a type
		- Resulted in a `tensor` of `dtype=torch.int64`
	- We can _work around_ this issue by specifying the type to use when we call the two `mean` methods
		- For example
			- `torch.mean(x.type(torch.float32))` or
			- `x.type(torch.float32).mean()`
- Pick a style for your calls
	- Either `torch.min(tensor)`
	- Or `tensor.min()`
	- I think I prefer the former (more functionaly)