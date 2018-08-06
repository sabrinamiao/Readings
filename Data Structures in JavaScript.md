# For Frontend Technical Interviews

## Stack

### Arguably the most important ***Stack*** in JavaScript is the ***call stack*** where we push in the ***scope*** of a function whenever we execute it

### Programmatically, it's just an array with two principled operations: push and pop. Push adds elements to the top of the array, while pop removes them from the same location. In other words, ***Stack*** follow the "Last In, First Out"(LIFO) protocol

## Queue

## JavaScript is an event-driven programming language which makes it possible to support non-blocking operations

## Internally, the browser manages only *one thread* to run the entire JavaScript code, using the event queue to enqueue listeners and the event loop to listen for the registered events

## Promises depend on this event-driven architecture to enable the seamless execution of asynchronous code that does not block other operations

## Programmatically, Queues are just arrays with two primary operations: unshift and pop. Unshift enqueues items to the end of the array, while pop dequeues them from the beginning of the array. In other words, Queues follow the "First In, First Out"(FIFO) protocol

## Linked List

## Like arrays, Linked lists store data elements in sequential order. Instead of keeping indexes, linked lists hold pointers to other elements. The first node is called the head while the last node is called the tail

## In a singly-liked list, a pointer to the previous node is also kept

## Liked lists have constant-time insertions and deletions because we can just change the pointers

## Linked lists can grow as long as there is space. However, even "dynamic" arrays that automatically resize could become unexpectedly expensive

## Linked list can operate as stacks and can also operate as queues

## Linked list are useful on both the client and server. On the client, state management libraries like Redux structure its middleware logic in a linked-list fashion. When actions are dispatched, they are piped from one middleware to the next until all is visited before reaching the reducers. On the server, web frameworks like Express also structure its middleware logic in a similar fashion. When a request is received, it is piped from one middleware to the next until a response is issued

# Binary Search Tree

## A tree is like a linked list, except it keeps references to many child nodes in a hierarchical structure, In other words, each node can have no more than one parent

## The Document Object Model(DOM) is such a structure, with a root html node that branches into the head and body nodes, which further subdivide into all the familiar html tags

## The Binary Search Tree is special because each node can have no more than two children. The left child must have a value that is smaller than or equal to its parent, while the right child must have a greater value
