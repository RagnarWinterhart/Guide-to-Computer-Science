# Algorithms
## Binary Search

Works by:
- Checking middle element, ``mid = low+(high-low)/2``
- If the target is smaller, search left half
- If the target is larger, search right half
- Repeat until target is found or there is nothing left to search
Only works on sorted collections. This is ``O(log n)``

## Insertion Sort
Builds a sorted collection one element at a time. 

For each element it:

- Compares it to the elements before it.
- Shifts larger elements right.
- Inserts elements in their proper place.

Simple and works well for small collections. But worse case is ``O(n^2)``


## Merge Sort
Breaks a collection into smaller pieces to then sort.

- Divides collection into halves.
- Keeps dividing until each section has only one element.
- Merges sections back together in order.

Runtime of ``O(n log n)``, which is much more efficient that insertion sort for large collections. 

# Data Structures

## Stack
A Last-In First-Out (LIFO) data structure, that literally creates a stack of elements, where the most recently added or ``pushed`` element is on top and then when you remove something that same top element is what gets removed or ``popped``. With stacks you can only every add to the top or take from the top. So for a stack of n length you'd have to pop n times to empty it. 

## Queue
A First-in First-out (FIFO) data structure, unlike stacks queues act like a queue or line at the grocery store. So the first enqueued element is the first element to be dequeued. 


# Symbol Tables
Symbol tables hold key-value pairs, where the key is used to find the value. 
## Hash Table
A hash table is a way of implementing a symbol table, by using a has function to convert a key into an index where the value can be stored. Allowing for searching, adding and removing, typically taking O(1) time.

Sometimes two keys can produce the same hash or index when this happens it is called collision and the table must have a way to handle it. 