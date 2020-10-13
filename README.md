# Extra Assignment: Implementing ArrayList

Now that you know how to implement a linked list, in this extra
assignment (optional) you implement a different kind of list data
structure called array list.

An array list can be thought of as a growable array. Internally, an
array is used to store the elements that have been added to the list.
That internal array has a certain capacity (size). Adding an element
when the internal array is completely full, leads to an internal
operation that grows the capacity of the internal array. First, a new
array is allocated with a higher capacity. Then, the elements of the
current array are copied into that newly created array. Finally, the
newly created array (which has now been populated) is used as the
storage array for the array list, and the old array is discarded. (The
JVM's garbage collector will free the memory of the old array that's
no longer used.) The array list doesn't have to be generic, it can be a String
array list, integer array list etc.

## Exercise 1

Implement an `add` method for your array list, using an operation to
grow the capacity of the internal array when it is full.

## Exercise 2

Implement a `get` method for your array list which returns the element
at a given index (an integer) if it exists. It is OK to throw an
exception (which one?) if the index is larger than the size of the
array list.

## Exercise 3

Show using timing measurements (see method
[System.nanoTime()](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/System.html#nanoTime()))
that the `get` operation of your array list is faster than the `get`
method of a linked list. Note that you will need lists with fairly
large numbers of elements. For example, you could try with 10'000 or
100'000 elements (or, perhaps even larger).

## Exercise 4

Implement more methods for your array list, such as `size`, `remove`,
and `find` (or `search`).

## Exercise 5

If you feel especially ambitious, you can attempt to implement the
`subList​(int fromIndex, int toIndex)` method. The purpose of this method is to
create a new list with copies of the elements between indices
`fromIndex` and `toIndex` of the current list. Modifications of one list 
should not affect the other.
