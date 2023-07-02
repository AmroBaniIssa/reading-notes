Stack:
A stack is a linear data structure that follows the Last-In-First-Out (LIFO) principle. It means that the last item inserted into the stack is the first one to be removed. Think of it like a stack of books where you can only remove the topmost book.

Operations of a stack typically include:
 -push(item): Adds an item to the top of the stack.
 -pop(): Removes and returns the top item from the stack.
 -peek(): Returns the top item from the stack without removing it.
 -isEmpty(): Checks if the stack is empty.
 -size(): Returns the number of items in the stack.

Queue:
A queue is also a linear data structure, but it follows the First-In-First-Out (FIFO) principle. It means that the first item inserted into the queue is the first one to be removed. Think of it like a queue of people waiting in line.

Operations of a queue typically include:
 -enqueue(item): Adds an item to the end of the queue.
 -dequeue(): Removes and returns the item from the front of the queue.
 -peek(): Returns the item from the front of the queue without removing it.
 -isEmpty(): Checks if the queue is empty.
 -size(): Returns the number of items in the queue.

 Here's an example implementation of the operations:

 (((class Stack {
  constructor() {
    this.items = [];
  }

  push(item) {
    this.items.push(item);
  }

  pop() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items.pop();
  }

  peek() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items[this.items.length - 1];
  }

  isEmpty() {
    return this.items.length === 0;
  }

  size() {
    return this.items.length;
  }
}
)))

(((let stack = new Stack();

console.log(stack.isEmpty()); // Output: true

stack.push(1);
stack.push(2);
stack.push(3);

console.log(stack.size()); // Output: 3
console.log(stack.isEmpty()); // Output: false
console.log(stack.peek()); // Output: 3

console.log(stack.pop()); // Output: 3
console.log(stack.pop()); // Output: 2

console.log(stack.size()); // Output: 1
console.log(stack.isEmpty()); // Output: false
console.log(stack.peek()); // Output: 1

console.log(stack.pop()); // Output: 1
console.log(stack.isEmpty()); // Output: true
console.log(stack.pop()); // Output: null
)))