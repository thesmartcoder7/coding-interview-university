<br><br>

# Quadratic O ( n<sup>2</sup> )

Once you have gone through the the linear time complexity, it is pretty easy to understand quadratic complexity.

The way you add complexities is like basic arithmetic. i.e If anything that runs with an O(n) complexity is nested inside another O(n) operation, this becomes an O(n<sup>2</sup>) operation and that is just that.

When it comes to this, you will notice that the number of operations increase relatively faster compared to linear time.

### Example:

Consider the list below:

```python

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    print(number)

```

Again, this would take linear time to complete. What if we were supposed to compare the every item of the list with all the items within the same list? This would mean to write a the first loop then run another loop inside it to handle the comparison.

i.e

```python

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    print(number)
    for item in number:
        print(number > item)

```

With the knowledge that loops run with a linear complexity, it is clear that these are two loops where one is nested within another. This means that their complexities are multiplied.

O(n) x O(n) = O(n<sup>2</sup>)


This approach to solving propblems can be very dangerous given that a person might end up nesting these more than twice. I am aware that there are problems that require this approach out there but is still isn't an efficient way to solve a problem. Refer to the Big O analysis chart.
