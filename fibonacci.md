Three way in Fibonacci Sequence

第一种方法是时间复杂度是指数级的 exponential time
第二种可以说是最好的方法, 每次移动a 和 b到下一个
第三种方法就是创建一个dp array，用了空间复杂度去节省时间复杂度

面试的时候,可以和面试官讨论说 万一这个数很大的话，会越界，这个时候，我们需要做一下边界处理
或者用double

```
def fibonacci1(n):
	if n == 1 or n == 2:
   		return 1
    return fibonacci1(n-1) + fibonacci1(n-2)

def fibonacci2(n):
	a,b = 1, 1
    for i in range(n-1):
		a, b= b, a + b
    return a

def fibonacci3(n):
	if n == 0:
    	return 0
    elif n == 1:
    	return 1
    else:
    	fib = [0, 1]
        for i in range(2, n+1):
        	fib.append(fib[i-2]+fib[i-1])
        return f1b[i]
        
```

