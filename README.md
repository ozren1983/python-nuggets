# python-nuggets

## Unpacking Generalizations

NOTE: Python 3.5+ only!

```* iterable unpacking operator```

```** dictionary unpacking operator```

Ordering of argument types in a function call: positional, keyword, \* or \*\*.

Unpacking is allowed inside tuple, list, set, and dictionary:

```
>>> *range(4), 4
(0, 1, 2, 3, 4)
>>> [*range(4), 4]
[0, 1, 2, 3, 4]
>>> {*range(4), 4}
{0, 1, 2, 3, 4}
>>> {'x': 1, **{'y': 2}}
{'x': 1, 'y': 2}
```

In dictionaries, later values will always override earlier ones:

```
>>> {'x': 1, **{'x': 2}}
{'x': 2}
```

Useful for merging multiple dictionaries.

```
>>> first = {'a': 5, 'b': 10}
>>> second = {'b': 6, 'c': 15}
>>> {**first, **second}
{'a': 5, 'b': 6, 'c': 15}
```

References:
https://www.python.org/dev/peps/pep-0448/