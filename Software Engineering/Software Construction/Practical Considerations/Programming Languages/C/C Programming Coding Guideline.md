## C-M-001: One assignment per line limit

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

Code readability improves maintainability.

