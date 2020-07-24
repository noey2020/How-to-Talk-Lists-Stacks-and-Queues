# How-to-Talk-Lists-Stacks-and-Queues

August 2, 2019

Definitions Even a 6 year-old Can Understand

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!

Hire me!

Abstract Data Types

An abstract data type (ADT) is a set of objects together with a set of 
operations. Objects can be integers, reals, and booleans, to name a few, and
have operations associated with them, and so do ADTs. For the set ADT, we might
have such operations as add, remove, size, and contains. Alternatively, we
might only want the two operations union and find, which would define a 
different ADT on the set.

The List ADT

We define a general list of the form A0, A1, A2, ..., AN-1. We say that the 
size of this list is N. We will call the special list of size 0 an empty list.

For any list except the empty list, we say that Ai follows(or succeeds) Ai-1
(i < N) and that Ai-1 precedes Ai(i > 0). The first element of the list is A0,
an the last element is AN-1. We will not define the predecessor of A0 or the
successor of AN-1. The position of element Ai in a list is i. Throughout this
discussion, we will assume, to simplify matters, that the elements in the list
are integers, but in general, arbitrarily complex elements are allowed (and
easily handled by a class template).

Associated with these "definitions" is a set of operations that we would like
to perform on the List ADT. Some popular operations are printList and makeEmpty,
which do the obvious things; find, which returns the position of the first 
occurrence of an item; insert and remove, which generally insert and remove some
element from some position in the list; and findKth, which returns the element
in some position (specified as an argument). If the list is 34, 12, 52, 16, 12,
then find(52) might return 2; insert(x,2) might make the list into 34, 12, x,
52, 16, 12 (if we insert into the position given); and remove(52) might turn 
that list into 34, 12, x, 16, 12.

Of course, the interpretation of what is appropriate for a function is entirely 
up to the programmer, as is the handling of special cases.

Simple Array Implementation of Lists

All these instructions can be implemented just by using an array. Arrays are 
created with a fixed capacity, the vector class, which internally stores an
array, allows the array to grow by doubling its capacity when needed. This 
solves the most serious problem with using an array - namely, that historically,
to use an array, an estimate of the maximum size of the list was required. This
estimate is no longer needed.

Simple Linked Lists

In order to avoid the linear cost of insertion and deletion, we need to ensure
that the list is not stored contiguously, since otherwise entire parts of the 
list will need to be moved.

The linked list consists of a series of nodes, which are not necessarily 
adjacent in memory. Each node contains the element and a link to a node 
containing its successor. We call this the next link. The last cell's next link
points to nullptr.

As we can see, in principle, if we know where a change is to be made, inserting
or removing an item from a linked list does not require moving lots of items,
and instead involves only a constant number of changes to node links.

August 18, 2019

Summary

This chapter describes the concept of ADTs and illustrates the concept with
three of the most common abstract data types. The primary objective is to 
separate the implementationof the ADTs from their function. The program must
know what the operations do, but it is actually better off not knowing how it
is done.

Lists, stacks, and queues are perhaps the three fundamental data structures in 
all of computer science, and their use is documented through a host of examples.
In particular, we saw how stacks are used to keep track of unction calls and 
how recursion is actually implemented. This is important to understand, not 
just because it makes procedural languages possible, but because knowing how
recursion is implemented removes a good deal of the mystery that surrounds its
use. Although recursion is very powerful, it is not an entirely free operation;
misuse and abuse of recursion can result in programs crashing.

I included some posts for reference.

https://github.com/noey2020/How-to-Talk-Linear-Regression

https://github.com/noey2020/How-to-Talk-Statistics-Pattern-Recognition-101

https://github.com/noey2020/How-to-Write-SPI-STM32

https://github.com/noey2020/How-to-Write-SysTick-Handler-for-STM32

https://github.com/noey2020/How-to-Write-Subroutines-in-C-Assembly-STM32

https://github.com/noey2020/How-to-Write-Multitasking-STM32

https://github.com/noey2020/How-to-Generate-Triangular-Wave-STM32-DAC

https://github.com/noey2020/How-to-Generate-Sine-Table-LUT

https://github.com/noey2020/How-to-Illustrate-Multiple-Exceptions-

https://github.com/noey2020/How-to-Blink-LED-using-Standard-Peripheral-Library

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!

Hire me!

Have fun and happy coding!
