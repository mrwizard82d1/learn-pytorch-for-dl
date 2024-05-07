- Two main ways to multiple matrices
	- Element-wise (matrices must have **identical** dimensions)
	- Matrix multiplication (dot product)
		- Matrices must have equal left rows and right item columns
		- 
- Use `torch.matmul()` function instead of calculating by-hand
- Beware of **shape errors**

## Two main rules of matrix multiplication

1. **Inner dimensions** must match
	1. For example, multiplying a (3, 2) x (3, 2) **fails**
	2. Multiplying a (3, 2) x (2, 3) succeeds
2. Resulting matrix has shape of **outer dimensions**
	1. (3, 2) x (2, 3) results in shape of (3. 3)
	2. (2, 3) x (3, 2) results in shape of (2, 2)
	3. 
## Shape errors

- Among the most common errors in deep learning
- Often corrected by using transposition
	- For example, `tensor_B.T`, is transposition of `tensor_B`
	- Switches axis (or dimensions) of a tensor
		- If `tensor_B`.shape is (3, 2)
		- Then `tensor_B.T.shape` is (2, 3)

