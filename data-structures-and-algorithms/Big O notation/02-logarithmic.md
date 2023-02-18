<br><br>

# Logarithmic O ( log n )
The logarithm is a very important concept to understand in Big O notation and in Data Structures and Algorithms. 

Remember this expression?&nbsp; <strong style="font-size: 2vw">log <sub>a</sub> b</strong>

Well . . . yes. It is very important. I know it looks math-related, and admittedly, it is. What does it have to do with computer science? How does it apply to data structures and algorithms?

<strong style="font-size: 2vw">log <sub>a</sub> b = c &nbsp;&nbsp;if and only if&nbsp;&nbsp; a<sup>c</sup> = b </strong> 

O(log n) in computer science is the same as O(log<sub>2</sub>n) . . . the base 2 is usually not written because in computer science the base is always assumed to be binary. 

Anyway . . . let's break it down in the context of the Big O notation. Consider the following:

log(1) = 0
<br>
log(2) = 1
<br>
log(4) = 2
<br>
log(8) = 3
<br>
log(16) = 4

See a pattern yet? If everything inside the brackets is 'n' and everything outside on the right side of the '=' is the exponent, it means that everytime n doubles, the exponent only increases by 1.

This is a very important relation to understand. It means that log n will only increase by a small amount even if n grows to be a huge number.

I challenge you to finish the relation above using big values for the exponent. You will notice that small increments of the exponent will result into huge values of n by a very big margin. If you reverse that, and try to bring it to Big O analysis, it basically shows that as the input increases, the number of operations required to compute or run the algorithm will only increase by a tiny bit. 

### Example:
Consider the list below:

```python

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

```

If you were asked to find the number 4, you can always run through the entire list checking every single item. That would be inefficient. The best way to handle this would be to divide this into two and check the two halves. If you find 4 in one half, the other half is totally useless and there is not need to go through it. This is the foundation of binary search ( concept to be covered later ). 

After the first operation, you will end up with half the list.
```python

first_half = [1, 2, 3, 4, 5] # 4 is in this first half therefore continue

second_half = [6, 7, 8, 9, 10] # 4 is not in this half therefore discard

numbers = [1, 2, 3, 4, 5]

```

You repeat the same process again for the second operation:
```python
first_half = [1, 2, 3] # 4 is not in this first half therefore discard

second_half = [4, 5] # 4 is in this half therefore continue

numbers = [4, 5]

```

Repeat the same procees again for the third operation:
```python
first_half = [4] # 4 is in this first half therefore continue

second_half = [5] # 4 is not in this half therefore discard

numbers = [4] # found 4.

```

If you we used the other appoach:
```python

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    if numnber == 4:
        return "Found 4"
        
```
This would run 4 times. The O(log n) operation ran 3 times. Now what if the 4 was located at the end of the list? 
```python 
numbers = [1, 2, 3, 10, 5, 6, 7, 8, 9, 4]
```

The for loop approach will run 10 times just to get to the 4 where as the log n operation will still run 3 times. This is why the logarithm is a very important concept to understand in the world of the Big O.
