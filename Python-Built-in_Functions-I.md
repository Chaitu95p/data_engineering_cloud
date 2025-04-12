
# 🐍 Python Built-in Functions Cheat Sheet

> 📘 Total: 68+ built-in functions  
> ✅ Includes examples, descriptions, return types  
> 🗂 Categorized for easier lookup

## 🧮 Math Functions

| Function   | Description                            | Return Type   | Example                      |
|------------|----------------------------------------|---------------|------------------------------|
| `abs()`    | Absolute value                         | `int` / `float` | `abs(-5)` → `5`              |
| `divmod()` | Quotient and remainder                 | `tuple`       | `divmod(10, 3)` → `(3, 1)`   |
| `pow()`    | Power, optionally modulo               | `int` / `float` | `pow(2, 3)` → `8`            |
| `round()`  | Rounds a number                        | `int` / `float` | `round(3.14)` → `3`          |
| `complex()`| Complex number from real & imag        | `complex`     | `complex(2, 3)` → `(2+3j)`   |

## 📊 Aggregation Functions

| Function | Description            | Return Type     | Example              |
|----------|------------------------|------------------|-----------------------|
| `max()`  | Largest element        | same as element  | `max([1, 2, 3])` → `3`|
| `min()`  | Smallest element       | same as element  | `min([1, 2, 3])` → `1`|
| `sum()`  | Sum of all items       | `int` / `float`  | `sum([1, 2, 3])` → `6`|

## 🔁 Iterator / Functional Utilities

| Function     | Description                          | Return Type       | Example                                |
|--------------|--------------------------------------|--------------------|-----------------------------------------|
| `iter()`     | Creates an iterator                  | `iterator`         | `iter([1, 2])`                          |
| `next()`     | Retrieves next item from iterator    | `any`              | `next(iter([10, 20]))` → `10`          |
| `aiter()`    | Returns asynchronous iterator        | `async iterator`   | `aiter(obj)`                            |
| `anext()`    | Retrieves next async item            | `awaitable`        | `await anext(aiter(obj))`              |
| `enumerate()`| Returns iterable of index & items    | `enumerate`        | `enumerate(['a', 'b'])`                |
| `filter()`   | Filters items with a function        | `filter`           | `filter(str.isalpha, 'abc123')`        |
| `map()`      | Applies function to items            | `map`              | `map(str, [1, 2])`                     |
| `zip()`      | Tuples from multiple iterables       | `zip`              | `zip([1, 2], [3, 4])`                  |

## 🔣 Type Conversion

| Function     | Description                      | Return Type     | Example                           |
|--------------|----------------------------------|------------------|------------------------------------|
| `int()`      | Converts to integer              | `int`            | `int("42")` → `42`                |
| `float()`    | Converts to float                | `float`          | `float("3.14")` → `3.14`          |
| `str()`      | Converts to string               | `str`            | `str(123)` → `"123"`              |
| `bool()`     | Converts to boolean              | `bool`           | `bool([])` → `False`              |
| `complex()`  | Converts to complex number       | `complex`        | `complex(1, 2)` → `(1+2j)`        |
| `list()`     | Converts to list                 | `list`           | `list("abc")` → `['a','b','c']`   |
| `tuple()`    | Converts to tuple                | `tuple`          | `tuple([1, 2])` → `(1, 2)`        |
| `dict()`     | Creates a dictionary             | `dict`           | `dict(a=1)` → `{'a': 1}`          |
| `set()`      | Creates a set                    | `set`            | `set([1, 2, 2])` → `{1, 2}`       |
| `frozenset()`| Immutable set                    | `frozenset`      | `frozenset([1, 2])`               |
| `bytes()`    | Immutable byte object            | `bytes`          | `bytes('hi', 'utf-8')`            |
| `bytearray()`| Mutable byte object              | `bytearray`      | `bytearray('hi', 'utf-8')`        |
| `memoryview()`| Memory view of object           | `memoryview`     | `memoryview(b'abc')[0]` → `97`    |

## 🔍 Introspection & Logic

| Function       | Description                         | Return Type | Example                        |
|----------------|-------------------------------------|-------------|---------------------------------|
| `all()`        | True if all elements true           | `bool`      | `all([1, True])` → `True`       |
| `any()`        | True if any element true            | `bool`      | `any([0, 1])` → `True`          |
| `hash()`       | Returns hash value of object        | `int`       | `hash('abc')`                   |
| `id()`         | Object memory address               | `int`       | `id(42)`                        |
| `isinstance()` | Checks object type                  | `bool`      | `isinstance(5, int)` → `True`   |
| `issubclass()` | Checks if class is subclass         | `bool`      | `issubclass(bool, int)` → `True`|
| `type()`       | Type of an object                   | `type`      | `type(5)` → `<class 'int'>`     |
| `callable()`   | Is object callable?                 | `bool`      | `callable(len)` → `True`        |
| `dir()`        | Object’s attributes/methods         | `list`      | `dir([])`                       |
| `vars()`       | Object's `__dict__`                 | `dict`      | `vars(object)`                  |

## 🔡 String & Format

| Function   | Description                   | Return Type | Example                          |
|------------|-------------------------------|-------------|-----------------------------------|
| `chr()`    | Character from Unicode code   | `str`       | `chr(65)` → `'A'`                |
| `ord()`    | Unicode code of character     | `int`       | `ord('A')` → `65`                |
| `ascii()`  | ASCII-safe representation     | `str`       | `ascii('ñ')` → `'\xf1'`         |
| `repr()`   | String representation         | `str`       | `repr([1, 2])` → `'[1, 2]'`      |
| `format()` | Formats a value               | `str`       | `format(3.14, ".2f")` → `'3.14'`|

## 📥 Input/Output

| Function   | Description                    | Return Type   | Example                         |
|------------|--------------------------------|----------------|----------------------------------|
| `print()`  | Prints output                  | `None`         | `print("Hello")`                |
| `input()`  | Reads user input               | `str`          | `input("Name: ")`               |
| `open()`   | Opens a file                   | `file object`  | `open("file.txt", "r")`         |

## 🧩 Object Handling

| Function       | Description                         | Return Type | Example                           |
|----------------|-------------------------------------|-------------|------------------------------------|
| `object()`     | Returns a new base object           | `object`    | `object()`                         |
| `staticmethod()`| Defines a static method            | `function`  | `staticmethod(func)`              |
| `classmethod()` | Defines a class method             | `function`  | `classmethod(func)`               |
| `property()`   | Getter/setter descriptor            | `property`  | `property(getter, setter)`        |
| `super()`      | Access superclass methods           | `super`     | `super().method()`                |

## 🧠 Code Execution

| Function   | Description                      | Return Type | Example                          |
|------------|----------------------------------|-------------|-----------------------------------|
| `eval()`   | Evaluates a Python expression    | `any`       | `eval("2 + 2")` → `4`             |
| `exec()`   | Executes Python code             | `None`      | `exec("x = 5")`                   |
| `compile()`| Compiles code                    | `code`      | `compile("2+2", "", "eval")`      |
| `globals()`| Returns global namespace         | `dict`      | `globals()["x"] = 42`             |
| `locals()` | Returns local namespace          | `dict`      | `locals()`                        |

## 🔁 Sequence Utilities

| Function     | Description                       | Return Type | Example                         |
|--------------|-----------------------------------|-------------|----------------------------------|
| `len()`      | Number of elements                | `int`       | `len("abc")` → `3`              |
| `reversed()` | Reverse iterator                  | `iterator`  | `reversed([1, 2, 3])`           |
| `sorted()`   | Sorted list from iterable         | `list`      | `sorted([3, 1, 2])` → `[1, 2, 3]`|
| `slice()`    | Slice object                      | `slice`     | `slice(1, 5, 2)`                 |

## 📚 Interactive Shell Utilities *(optional)*

| Function      | Description                     | Return Type | Example           |
|---------------|---------------------------------|-------------|--------------------|
| `copyright()` | Shows copyright info            | `None`      | `copyright()`      |
| `credits()`   | Shows contributors info         | `None`      | `credits()`        |
| `license()`   | Shows license info              | `None`      | `license()`        |
