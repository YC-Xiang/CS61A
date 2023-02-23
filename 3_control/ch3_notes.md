> Windows use python to substitute python3

# Using Python

exit python: `exit()` or`Ctrl-D`

open an interactive session: `python3 -i lab00.py`

Runs doctests in a particular file: `python3 -m doctest lab00.py`

# Using OK

`python3 ok -q <specified function>`

By default, only tests that did not pass will show up. You can use the `-v` option to show all tests, including tests you have passed:

`python3 ok -v`

You can also use the debug printing feature in OK by writing

`print("DEBUG:", x)`

Finally, when you have finished all the questions in [lab01.py](https://inst.eecs.berkeley.edu/~cs61a/fa22/lab/lab01/lab01.py), you must submit the assignment using the `--submit` option:

`python3 ok --submit`

# Notes

**Truthy and Falsey Values**: It turns out `and` and `or` work on more than just booleans (`True`, `False`). Python values such as `0`, `None`, `''` (the empty string), and `[]` (the empty list) are considered false values. *All* other values are considered true values.



# lab01

### control

`python3 ok -q control -u`

### short-circuit

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

