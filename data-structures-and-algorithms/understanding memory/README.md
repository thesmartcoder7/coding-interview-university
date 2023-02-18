# Understanding Mermory

Memory is one subject that is not as easy to go through in summary but in the context of coding invterviews, it is something that can help shed some light to how data structures interact with memory and how space complexity come in.

Just to get this out of the way, there is no computer on the planet that has infinite memory. This means that memory, just like most things, is bounded ( finite ). Therefore, you can get to a point where you run out of memory.

The most basic thing you will every do in a coding interview is defining a variable and accessing that variable. Something like:

```python
age = 25
```

The simple act of declaring a variable like this uses up memory. Could be random or not. I can go into the intricacies of how the computer allocates memory but it is not that relevant in the context of coding interviews. The key take away on this is that a variable is stored in memory. And it could be a single memory slot or more depending on the data structure you choose to use in your code.

Now if this variable 'age' was a list of different age values, they would be stored back to back. This means that the computer would allocate contiguous memory slots to the variable. And please understand that in this case, I am giving an example of an array of age values like:

```python
ages = [30, 42, 20, 41, 23]
```

Each value would be store back to back in memory. Now. some data structures like linked lists use a different approach to saving data but You will understand more how this works when you go over the linked list section.

It is good to undestand that data is present as binary under the hood because that is the language the computer understands. The basic unit of memory is the bit. zeros ( 0 ) and ones ( 1 ).

One memory slot holds 8 bits. that means one memory slot is one byte.

```python
0000 0000 = byte
0 = bit
```

Every bit moving from the right to the left represents a new power of 2. i.e 

0&nbsp;&nbsp; &nbsp;&nbsp;0&nbsp;&nbsp; &nbsp;&nbsp;0&nbsp;&nbsp; &nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0&nbsp;&nbsp; &nbsp;&nbsp;0&nbsp;&nbsp; &nbsp;&nbsp;0&nbsp;&nbsp; &nbsp;&nbsp;0
<br>
2<sup>7</sup>&nbsp;&nbsp;&nbsp;2<sup>6</sup>&nbsp;&nbsp;&nbsp;2<sup>5</sup>&nbsp;&nbsp;&nbsp;2<sup>4</sup>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2<sup>3</sup>&nbsp;&nbsp;&nbsp;2<sup>2</sup>&nbsp;&nbsp;&nbsp;&nbsp;2<sup>1</sup>&nbsp;&nbsp;&nbsp;&nbsp;2<sup>0</sup>


Basically, any piece of data can be transformed into binary, and then it will we stored in bytes, which are stored in memory slots.

Going back to the number example, the biggest number that can fit into one byte is 256. And this is where needing more memory slots comes in. If you have data that can't fit into one byte of memory, the computer saves allocates more free memory slots for it back to back.

It is also very important to undestand that memory slots don't just store your basic data like strings, arrays, numbers e.t.c, it can also store memory addresses that belong to other memory slots, and this is where the concept of pointers come in. This is a very important concept because of data structures like the linked list. With this, you no longer have to have contiguous memory, you can simply point to another memory slot where the data is actually store. This is the basics of the linked list and you will cover it in detail when you visit the link to that section.



