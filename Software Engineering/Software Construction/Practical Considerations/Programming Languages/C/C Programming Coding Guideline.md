## C-M-001: One Assignment Per Line Limit

Multiple assignment on a single line are not allowed.

### Examples

Compliant:

``` C
a = c:
b = c;
```

``` C
b += 1;
a = b + 2;
```

``` C
b++;
c++;
a = b + c;
```

Non-compliant:

``` C
a = b = c;
```

``` C
a = (b += 1) + 2;
```

``` C
a = (b++) + (c++);
```

### Reasoning

Readability is generally better when only taking one action per line.

Chaining of assignments can break if the types of the variables are changed in a future implementation.
