## C-M-001: One assignment per line limit

Maximum one assignment per statement is allowed.

### Discussion

Having multiple assignments in a line of code impairs code readability. Note that besides the simple assignment (=), the rule also include the compound assignments (+=, -=, etc), as well as the increment and decrement operators (++, --) due to that these de facto also assign a value to a variable.

### Exceptions

Multiple assignments may be used in one statement if to assign multiple variables to one single value. This is due to that the other option, to split the assignments over multiple rows, is deemed to have inferior code readability in this special case.

### Compliant Example

``` C
a = b = c = 0;    // Compliant due to exception to the rule.
```

### Non-compliant Examples

``` C
a = (b += 1) + 2; 
```

``` C
a = (b++) + (c++);
```
