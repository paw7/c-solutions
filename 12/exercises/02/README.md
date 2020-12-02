### Exercise 12.02
Suppose that `high`, `low` and `middle` are all pointer variables of the same
type, and that `low` and `high` point to elements of an array. What is the
following statement illegal, and how could it be fixed?

```c
middle = (low + high) / 2;
```

### Solution

 The statement is illegal because pointers cannot be added. Here's a legal statement that has the desired effect:
 The value of (high - low) / 2 is an integer, not a pointer, so it can legally be added to low.

```c
middle = low + (high - low) / 2;
```
