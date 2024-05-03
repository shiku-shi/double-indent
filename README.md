# double-indent-shiku

A code formatter to add double indentation to function and method definitions,
also calls in `if` and `for` statements. Original repository:
https://github.com/theendlessriver13/double-indent/

Forked to met internal formatting requirements. Meant to be used after
[black](https://github.com/psf/black).

## Installation

`pip install double-indent-shiku`

## usage

```console
usage: double-indent [-h] [-i INDENT] [filenames ...]

positional arguments:
  filenames

optional arguments:
  -h, --help            show this help message and exit
  -i INDENT, --indent INDENT
                        number of spaces for indentation
```

## indent function and method definitions twice

```diff
 def func(
-    arg,
-    arg2,
+        arg,
+        arg2,
 ):
     ...
```

```diff
 class C:
     def __init__(
-        self,
-        arg,
+            self,
+            arg,
     ):
         ...
```

```diff
for value in values(
-   arg,
-   arg2,
+       arg,
+       arg2,
):
    ...
```

```diff
if values(
-   arg,
-   arg2,
+       arg,
+       arg2,
):
    ...
```
