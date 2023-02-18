<br><br>

# Constant O ( 1 )
Suppose a borrow the same list from the first example.
```python

my_list = ['-']

print(my_list[0]) # O(1)
        
```

If I were to print this, I will only need to run this once. This does will remain the same regardless of the number of items I have in the list.

i.e 
```python

my_list = [ '-', '/', '*', '+' ]
 
print(my_list[0]) # O(1)
        
```

See, regardless of the number of items I have in the list, it will still take the same number of operations to get the first element. This is what is called Constant time.

