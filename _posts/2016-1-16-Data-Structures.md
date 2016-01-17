---
layout: post
title: Design Patterns of Common Data Structures 
---

JavaScript has two built-in data structures that come out of the box - arrays and objects. There are many differently behaving data structures that can be created. The preferred one to be used should be determined by:

1. What sort of actions will be most performed, e.g., access (finding a value when given an id), search (identify a particular value), insertion, and deletion.

2. Which data structure offers the lowest order time complexity for those actions

So what sort of data structures are there?

This list is hardly conclusive, but it contains many of the common data structure design patterns that are used. They behave and interface with the user in a variety of ways. 


##Some data structures and their design patterns:

**Stacks** - A linear data structure, where both access and insertion can only occur from the 'top' of the stack. Imagine a stack of dinner plates, where you can only access, add and remove a plate from the top of the stack. Last in, First out (the last plate put on top is the first plate removed from the top).


**Queues** - A linear data structure where values can only be inserted to the 'back' and where access and removal can only occur from the 'front'. First in, First out (first to wait in line is the first to exit the line).


**Linked Lists** - Another linear structure where each value is held in a separate object (or 'node') that also has a property that references the next node in the list. A 'doubly linked list' is a linked list where those nodes also contain a property referencing the previous node as well. There are also usually a 'head' and 'tail' that reference the first and last node in the list, respectively. An insertion can be made anywhere in a link list by simply creating a new node with the value, and changing both the 'next' and 'previous' references of both the nodes before and after where the desired insertion will occur.


**Trees** - Trees are structures that consist of many layers nodes, where a parent node will reference child nodes, which themselves can reference child nodes, and so on. Each individual node is a tree in itself since it also contains a value and can possess its own children. Binary trees are trees where each parent node can have up to two child nodes.



**Hash Tables** - Hash tables are structures that are used to store keys and values in a limited array, or an array that has a fixed size at any given time. It does so by running a special hash function that runs a randomizing algorithm to convert they keys to indices, and then stores the values in those corresponding indices (or buckets) in a [key, value] pair that is commonly called a 'tuple'. The limited array's size must be fixed at any given time so that a valid index can be produced by the hash function. ***There are several ways to deal with hash collisions*** - or what happens when two different keys passed through the hash function return the same index:


* One such way is called *"chaining,"* and this solves the collision by storing multiple tuples in a single index of the limited array. When two different keys both hash to the same index, BOTH will be stored in the same index by pushing to an array of tuples at that index (or alternately, a linked list). 


* A second way to deal with collisions, is that when a key hashes into an already filled index/bucket, it simply looks for a different index/bucket to occupy. This can be done by simply incrementing the index until an empty bucket is found - this is called *linear probing*. Another way to determine a different index to use, is to have a second hash function return a random value that can be added to the index, but still be within the bounds of the limited array - this is called *double hashing*. 


* Finally, another way to lessen the number of collisions is to have a dynamically resizing hash table. The greater the ratio of the hash table size to the number of values to be stored, the less likely that collisions will occur. The table needs to be resized larger as the number of values approaches the length of the limited array.


Tomorrow, I will take a look into how the designs of these different data structures, and how the time complexity of specific operations will effect which one would be best for a given situation.

