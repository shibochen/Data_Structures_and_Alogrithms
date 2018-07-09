# Deque

`Deque` is a Queue-like data structure that supports insertion and deletion at the both the front and back of the queue

Deque is an interface and has two implementations:
1. LinkedList
2. ArrayDeque

`Deque dq = new LinkedList()`;

`Deque dq = new ArrayDeque()`;

## ArrayList vs ArrayDeque
ArrayDeque has the ability to add or remove the elements from both ends (head or tail), on the other hand 
removing last element from ArrayList takes O(n) time as it traverses the whole list to reach the end. So if you want to 
add or remove elements from both ends choose ArrayDeque over ArrayList,however if you only want to perform the opreation 
on the tail (at the end) then you should choose ArrayList


## Method
![deque](https://user-images.githubusercontent.com/38870192/42431087-4ae34e28-8311-11e8-878f-3fda3d147be5.PNG)


## Reference
- [Data Structure and Algorithm in Java Page 248](x)
