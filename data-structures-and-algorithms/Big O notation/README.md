# Introduction to the Big O

The official full definition of the Big O is Big O assymtotic analysis.
This doesn't just focus on solving problems, it focuses more on how well
the problem is solved. This is how you separate good code from normal code, great code from good code and god-tier code from great code.

## What is good code?

Good code can be describe using two main factors:

- Scalability
- Readability

Big O looks more into the first one. Scalability. Scalability in this context basically means "Will you code still run or peform with the same efficiency if the input is increased" ?

### Example:

Suppose you write a function to find a dash (` - `) from a list of characters.

```python

my_list = ['-']

for item in my_list:
    if item == '-':
        print("Found the Dash!")

```

If you were to run this program, you will notice that this executes relatively fast. I should. I mean, it is only running once, right? . . . But what if the items in the array were more than 100,000? You will notice that the same number of lines of code would take much longer to execute. This is because this piece of code runs as many times as the number of items in the list/array. ( This, right here, is the foundation of the Big O )

Keep in mind that this will run with a different speed on different computers depending on a lot of factors like, speed of the processor, if more apps are open in the background or not e.t.c Big O notation is the language used for talking about how long a program takes to run.

I know this might be a little bit confusing. Tip, don't focus on the time. Big O focuses on the number of operations done to peform the function. To bring this home, the function above will run only once if the list has only one item. However, it will run as many times as the number of items in the list. Since Big O looks at the worst case scenario, you'd say that the number of operations will increase as the size of the input increases, which will be O(n).

So what causes this inconsistencies and different Big O notations? The most common culprits to this are:

For time complexities:
- Operations
- Comparisions
- Loops
- Outside Function calls.

For space complexities:
- Creating Variables
- Data Structures
- Function calls
- Allocations

There are different ways you can analyze your efficiency. This chart breaks it all down.

![Big O Image](assets/big-o-chart.jpeg)

## Big O Analysis

- [Constatnt - O(1)](01-constant.md)
- [Logarithmic - O(log n)](02-logarithmic.md)
- [Linear time - O(n)](03-linear.md)
- [Log-Linear - O(n log n)](04-log-linear.md)
- [Quadratic - O(n<sup>2</sup>)](05-quadratic.md)
- [Exponential - O(2<sup>n</sup>)](06-exponential.md)
- [Factorial - O(n!)](07-factorial.md)

Remember, time complexity is the measure of how fast an algorithm runs where as space complexity is the measure of how much auxiliary memory an algorithm takes up.
