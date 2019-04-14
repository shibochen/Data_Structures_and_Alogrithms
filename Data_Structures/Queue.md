# Queue

`Queue` is a linear data structure in which the operations are performed on **First-in-First-out(FIFO)** principle.

```java
Queue<Integer> queue = new Queue<Integer>();
```

**Note**: `java.util.Queue` is an interface so you cannot instantiate it directly. You can instantiate class.

## Implementations

1. LinkedList
2. PriorityQueue

```java
Queue q1 = new LinkedList();
Queue q2 = new PriorityQueue();
```

## Basic Methods

- **offer**
- **poll**
- **peek**
- **isEmpty**
- **size**

## Priority Queue

Priority Queue is an extension of queue with following properties.

1. Every item has a priority associated with it
2. An element with high priority is dequeued before an element with low priority
3. If two elements have the same priority, they are served according to their order in the queue

## Implementation

1. Array
2. Heap