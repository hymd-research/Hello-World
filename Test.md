

Written with [StackEdit](https://stackedit.io/).

## Memorizing

> Recursive function with memorizing written in Python.

```Python
def memorize(f):
	MEMO = dict()
	def function(n):
		if n not in MEMO.keys():
			MEMO[n] = f(n)
		return MEMO[n]
	
	return function

@memorize
def fib(n):
	return n if 0 <= n < 2 else 0 if n < 0 else fib(n-1) + fib(n-2)
```

