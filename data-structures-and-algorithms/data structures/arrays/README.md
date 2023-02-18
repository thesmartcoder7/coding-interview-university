# Introduction to Arrays

An array / list is a data structure that arranges data one after the other in memory ( They are stored in contiguous memory i.e in order ). It is the simplest and most widely used data structure.

There are two types of arrays. The static array and the dynamic array. At a very high level, a static array is one that has a fixed length and therefore immutable, where as a dynamic one's length is not fixed and therefore mutable. ( Will discuss this further down the document )

With any type of array, there are two main operations that run with a constant time complexity O( 1 ). There are the:

- get / access / read
- set / update / edit

There two run with constant time because you are only accessing one element in the array. The number of operations for this will not change no matter the size of the array.

```python
    numbers = [1, 2, 3 ,4 , 5]
```

If you want to access the third item from the array, you need only specify the index. i.e numbers[2]. This also works for when you are trying to change the value at the third index. ie. numbers[2] = 7

What time complexity does initializing an array run on? Suppose you initialize an array

```python
my_numbers = [1, 2, 3, 4, 5 ]
```

Since you are saving this in memory and each one of these items like take 8bits in memory, you end up runing (8 \* n) operations to store the full array. Ergo, the time complexity and space complexity for initializing an array will always be O( n )

How about traversal? What if I was to print every item in the array once? This will require the use of a for loop.

```python
    for number in my_numbers:
        print(number)
```

Everytime the loop runs print is fired. If print is an O( 1 ) operation and runs for as many times as the number of items then the total complexity is &nbsp; &nbsp;<strong>O( n \* 1)</strong> &nbsp; &nbsp;time and &nbsp; &nbsp;<strong>O( 1 )</strong> &nbsp; &nbsp;space. For that, it is safe to say that for traversing an array, the Big O notation is simply &nbsp; &nbsp;<strong>O( n )</strong> &nbsp; &nbsp;for time and &nbsp; &nbsp;<strong>O( 1 )</strong> &nbsp; &nbsp; space.

Another operation done on arrays is copying. This usually accompanies something like insertion. To understand it let me cover insertion first. Now insertion is basically as the word describes it. It is where you have an array of length x and you want to add another element into it so that the length becomes x + 1. Now you can either insert the item at the beginning of the array, somewhere in the middle or at the end which is basically appending.

Anytime you append an item into an array, the operation will be O( 1 ) for a dynamic array and O( n ) for a static array. Let me explain. For a static array, the length is fixed and the so is the me memory slot allocated to the array. If you add something new, there is no wiggle room to accomodate the extra item ergo, the computer copies the original array under the hood and looks for another location where the slots are contiguous so that it can store the copied array plus the new item. This is an operation of O( n ) for both time and space. for inserting however the space complexity is constant O( 1 ). This is because even though the computer is copying the old array and re-saving the new array, it is also freeing up the memory occupied by the original array before insertion. With that, I believe the Big O analysis for both copying and inserting are clear.

Now that the concept of static array is covered, dynamic arrays are pretty simple. What you should know is that whatever the length of your declared array, the computer allocated twice as much space. This means that you have even faster time for appending. If you happen to fill the allocated space, then and only then will the computer copy this full array to another memory location while giving you twice as much space as what is needed by the new array. For this, inserting elements at the end of the array will always be an operation of O( 1 ) for both time and space

This concept of inserting something at the end, middle and beginning of the array applies also for deletion. If you delete an item from the end of the array, the operation is considered to be O( 1 ) for both space and time. For removing items at the beginning or in the middle of the array, the operaiton becomes one of O( n ) time and O( 1 ) space.

## Space complexity summary for Arrays:
- get / access / read = O( 1 )
- set / update / edit / write = O( 1 )
- insert = O( n )
- delete = O( n ) 
- copying = O( n )