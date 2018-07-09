# Queue

`Queue` is a linear data structure in which the insertion and deletion operations are performed on **First-in-First-out(FIFO)** principle. 

`Queue<Integer> queue = new Queue<Integer>();` <br />
`java.util.Queue` is an interface so you cannot instantiate it directly. You can instantiate class.

Queue interface in Java collections has two implementations:
1. LinkedList
2. PriorityQueue

`Queue q1 = new LinkedList();` <br />
`Queue q2 = new PriorityQueue();` <br />

## Methods for Queue interface

| Method | Description | 
| :---: | :---:|
| offer(object) | Inserts the specified element into the queue
| poll() | It is almost same as **remove** method. The only difference between them is that **poll()** method returns null if the Queue is empty |
| peek() | It is almost same as **element()** method. The only difference between them is that **peek()** method returns null if the Queue is empty |
| add(object) | Adds the specified element into the queue |
| remove() | Removes the head (first element) of the Queue and return its value |
| element() | Returns the head (the first element) of the Queue |
| isEmpty() | Check if the queue is empty or not |
| size() | Get the size of the queue |

## Queue Method Table
![capture2](https://user-images.githubusercontent.com/38870192/42430805-80b9766e-830f-11e8-85a7-73d4d6341d3d.PNG)

![queuemethods](https://user-images.githubusercontent.com/38870192/39684074-4f0fdb30-5187-11e8-893e-90f432abf62d.PNG)


## Reference
- [Data Strcuture and Algorithm in Java Page 240](x)
- [Queue Interface In Java](https://www.geeksforgeeks.org/queue-interface-java/)
