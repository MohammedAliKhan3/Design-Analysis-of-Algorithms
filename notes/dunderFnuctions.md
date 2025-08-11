# Dunder Methods in Python

"Dunder" functions (short for "double underscore") are special methods in Python that get automatically called when certain actions happen to an object of that class. They're like hooks into Python's syntax and built-in behavior.

## Common Dunder Methods

| Dunder Method    | When It's Called                          | Example                   |
|------------------|------------------------------------------|---------------------------|
| `__init__`       | When you create an object                | `h = Heap(10)`            |
| `__str__`        | When you print or convert to string      | `print(h)`                |
| `__len__`        | When you call `len()` on it              | `len(h)`                  |
| `__getitem__`    | When you use `obj[index]`                | `h[0]`                    |
| `__setitem__`    | When you assign with `obj[index] = value`| `h[1] = 5`                |
| `__call__`       | When you treat the object like a function| `h()`                     |
| `__del__`        | When the object is destroyed             | `del h`                   |
| `__iter__`/`__next__` | When you loop over it               | `for x in h:`             |

## How They Work

- When you do certain operations on an object, Python checks if your class defines the corresponding dunder method
- If defined, Python calls it automatically
- If not defined, Python uses default behavior

## Key Points

1. Dunder methods enable operator overloading
2. They allow your objects to integrate with Python's built-in functions
3. They provide hooks into Python's core language features
4. The names are always surrounded by double underscores
