# C99 printf vs Python print Formatting Comparison

This document demonstrates how to format integers, floats, and strings in C99 and Python.
Proper formatting ensures clear, readable output.

> formatting output matters, as without it can make your work appear less import, and meaningful. Plus it is a very handy tool to use in software dev work, it will benefit you later in life.

<hr>

## Integer Formatting

### C99 printf

```c
#include <stdio.h>
int main()
{
int n = 42;
printf("%5d\n", n); // width 5, right-aligned
printf("%+5d\n", n); // width 5, show sign
printf("%05d\n", n); // width 5, pad with zeros
return 0;
}
```

#### Output:

```c
42
+42
00042
```

### Python print

#### Old-style (%) formatting

```python
n = 42
print("%5d" % n) # width 5, right-aligned
print("%+5d" % n) # width 5, show sign
print("%05d" % n) # width 5, pad with zeros
```

#### F-strings

```python
n = 42
print(f"{n:5}") # width 5, right-aligned
print(f"{n:+5}") # width 5, show sign
print(f"{n:05}") # width 5, pad with zeros
```

#### Output:

```c
42
+42
00042
```

## Float formatting

### C99 printf

```c
#include <stdio.h>
int main()
{
float f = 3.14159;
printf("%8.2f\n", f); // width 8, 2 decimals
printf("%08.2f\n", f); // pad with zeros
printf("%e\n", f); // scientific notation
return 0;
}
```

#### Output:

```c
3.14
00003.14
3.141590e+00
```

### Python print

#### Old-style (%) formatting

```python
f = 3.14159
print("%8.2f" % f)
print("%08.2f" % f)
print("%e" % f)
```

#### F-strings

```python
f = 3.14159
print(f"{f:8.2f}")
print(f"{f:08.2f}")
print(f"{f:e}")
```

#### Output:

```python
3.14
00003.14
3.141590e+00
```

## String Formatting

### C99 printf

```c
#include <stdio.h>
int main() {
char *s = "Hello";
printf("%-10s!\n", s); // left-aligned, width 10
printf("%10s!\n", s); // right-aligned, width 10
return 0;
}
```

#### Output:

```c
Hello    !
Hello!
```

### Python print

#### Old-style(%) formatting

```python
s = "Hello"
print("%-10s!" % s)
print("%10s!" % s)
```

#### F-strings

```python
s = "Hello"
print(f"{s:<10}!")
print(f"{s:>10}!")
print(f"{s:^10}!")
```

#### Output:

```python
Hello   !
   Hello!
Hello   !
```

## Comparison Table

| Type   | Example Code (C)           | Example Code (Python) | Output       |
| ------ | -------------------------- | --------------------- | ------------ |
| int    | printf("%5d", 42);         | "%5d" % 42            | 42           |
| int    | printf("%+5d", 42);        | "%+5d" % 42           | +42          |
| int    | printf("%05d", 42);        | "%05d" % 42           | 00042        |
| float  | printf("%8.2f", 3.14159);  | "%8.2f" % 3.14159     | 3.14         |
| float  | printf("%e", 3.14159);     | "%e" % 3.14159        | 3.141590e+00 |
| string | printf("%-10s!", "Hello"); | "%-10s" % "Hello"     | Hello !      |
| string | printf("%10s!", "Hello");  | "%10s" % "Hello"      | Hello!       |

## Useful Links

- [C99 printf documentation](https://en.cppreference.com/w/c/io/fprintf)
- [Python old-style % formatting](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)
- [Python f-strings
  ](https://docs.python.org/3/reference/lexical_analysis.html#f-strings)

## Image

![Markdown Logo](https://www.mtech.edu/montana-true/files/mt-web.jpg)

## Additonal Requirements

- use `<hr>` to seperatemahor sections $\checkmark$
- use `lists` $\checkmark$
- Include `at least one image` $\checkmark$
- Use `inline code` $\checkmark$
- Ensure `proper indentation and spacing` $\checkmark$
