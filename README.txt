### Subtraction Function

The `subtract()` function subtracts one number from another. It can be used whenever the difference between two numbers is needed.

The function may break or give an error if non-numeric values, such as text, are provided.

Example:

```python
def subtract(a, b):
    result = a - b
    return result

subtract(10, 4)  # Returns 6
```

### distance_from_zero(x)

The function calculates how far a number is from zero. It calls the existing `subtract()` function and always returns a positive distance.

The function may give an error if a non-numeric value, such as text, is provided.

Example:

```python
def distance_from_zero(x):
    if x >= 0:
        return subtract(x, 0)
    else:
        return subtract(0, x)

distance_from_zero(-4)  # Returns 4
```


## add(a, b)

Adds two numbers together and returns the result.

**Parameters:**
- `a`: first number (int or float)
- `b`: second number (int or float)

**Returns:** the sum of `a` and `b`

**When it might break:**
- Passing non-numeric types (e.g. strings, lists) will raise a `TypeError`
- Very large numbers may lose precision due to floating-point limitations

**Example:**
```python
add(2, 3)      # returns 5
add(-3, 5)     # returns 2
add(5, 8)      # returns 13
```

## sum_list(values)

The `sum_list()` function adds all numbers in a list together. It can be used whenever the total of multiple numbers is needed.

The function may break or give an error if non-numeric values, such as text, are provided.

Example:

```python
def sum_list(values):
    total = 0
    for value in values:
        total = add(total, value)
    return total

sum_list([1, 2, 3, 4])  # Returns 10

#Multiply 

The function is used when calculating the product between two numbers 

#when it might break 
If a or b is non-numeric types (e.g. strings, lists) will raise a `TypeError`

Example:
''' python
def multiply(a,b):
    result = a * b
    return result

multiply(1,2)  #returns 2
'''
## square(x)

The function is used when calculating the square of a number (multiplying it by itself). It relies on the `multiply` function internally

**When it might break:**
If `x` is a non-numeric type (e.g. strings, lists), it will raise a `TypeError` — since it depends on `multiply`, it inherits the same failure cases.

**Example:**
```python
def square(x):
    return multiply(x, x)

print(square(3))    # returns 9
print(square(5))    # returns 25
print(square(-2))   # returns 4
```
