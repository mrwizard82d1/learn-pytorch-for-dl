- PyTorch provides methods to find these values
	- Similarly, if `tensor = torch.arange(1, 100, 10)`
	- Call
		- `torch.argmin(x)` or `x.argmin()` both return `tensor(1)`
		- `torch.argmax(x)` or `x.argmax()` both return `tensor(10)`