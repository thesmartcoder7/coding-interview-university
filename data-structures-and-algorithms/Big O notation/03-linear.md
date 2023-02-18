<br><br>

# Linear O ( n )
When you think about the linear time complexity, you should be thinking about proportionality. That is the simplest way to have it. By that, I mean  the number of operations required to run the program is directly proportional to the size of the input.

### Example:
Consider the list below:

```python

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

```
If you were asked to loop through this array/list and print out every single item, it will take you the same number of operations as the number of items in that array/list to complete the program.

```python

for number in numbers:
    print(number)

```

This is the simple solution to it. If this list only had two items, the program would run two for loops for it. If there were five items, it will run five times . . . and so on.

O(n) is really considered a fair speed but that is if you don't have nested for loops. 

The way you add complexities is like basic arithmetic. i.e If anything that runs with an O(n) complexity is nested inside another O(n) operation, this becomes an O(n<sup>2</sup>) operation and that is just that. 

