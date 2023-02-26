# Lecture

## Print and None

```python
>>> print(print(1), print(2))
1
2
None
None
# cuz print return None
```

## Multiple Environments

## Miscellaneous Python Features

```python
# multiple return value
def divide_exact(n ,d):
    return n // d, n%d
>>> quotient, remainder = divide_exact(2013, 10)
>>> quotinent
201
>>> remainder
3
```

## Conditional statements

False values in Python: `False 0 '' None`

True values in Python: Anything else(True)

# Textbook

### 1.5.6 Testing

**Assertions.** When the expression being asserted evaluates to a true value, executing an assert statement has no effect. When it is a false value, assert causes an error that halts execution.

```python
assert fib(8) == 13

>>> def fib_test():
        assert fib(2) == 1, 'The 2nd Fibonacci number should be 1'
        assert fib(3) == 1, 'The 3rd Fibonacci number should be 1'
        assert fib(50) == 7778742049, 'Error at the 50th Fibonacci number'

```

**Doctests.**

```python
# testmod 测试整个文件的doctest
>>> from doctest import testmod
>>> testmod()
TestResults(failed=0, attempted=2)
```

```python
# run_docstring_examples 运行指定函数的doctest. sum_naturals：函数名。globals()：global environment。True：打印详细信息。
>>> from doctest import run_docstring_examples
>>> run_docstring_examples(sum_naturals, globals(), True)
```



# Lab

> Windows use python to substitute python3

## Using OK

To use Ok to run doctests for a specified function, run the following command:

`python3 ok -q <specified function>`

By default, only tests that did not pass will show up. You can use the `-v` option to show all tests, including tests you have passed:

`python3 ok -v`

You can also use the debug printing feature in OK by writing

`print("DEBUG:", x)`

Finally, when you have finished all the questions in lab01.py, you must submit the assignment using the `--submit` option:

`python3 ok --submit`

## Control

`python3 ok -q control -u`

### short-circuit

**Truthy and Falsey Values**: It turns out `and` and `or` work on more than just booleans (`True`, `False`). Python values such as `0`, `None`, `''` (the empty string), and `[]` (the empty list) are considered false values. *All* other values are considered true values.

`python3 ok -q short-circuit -u`

```python
>>> True and 13
13
# If and and or do not short-circuit, they just return the last value; another way to remember this is that and and or always return the last thing they evaluate, whether they short circuit or not.
```

```python
>>> False or 0
0
# wrong:False
# reason as above. In python 0 not equal False
```

```python
>>> True and 0
0
```

