Recursivity is a programming techniques that is similar to [[loop]] where a function call itself **recursively** (multiple times)

```python
def factorial(n):
	"""
	Compute the factorial of a number
	"""
	if n == 0 or n == 1: 
		return 1 
	else: 
		return n * factorial(n - 1)
```
