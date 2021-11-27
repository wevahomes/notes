# Stacks and Queues - Main

---

## Implementing a Stack

---

- (*) Stacks and queues.
- (1) What is a stack and what is it an alternative to?

<details>

- (1)
    - A stack is a data structure.
    - It is an alternative to an array.

</details>

---

- (*) Stacks and queues.
- (1) What ordering does a stack use?

<details>

- (1) A stack uses LIFO (last-in first-out) ordering.

</details>

---

Detail four stack operations.

<details>

- pop(): Remove the top item from the stack.
- push(item): Add an item to the top of the stack.
- peek(): Return the top of the stack.
- isEmpty(): Return true if and only if the stack is empty.

</details>

---

Compare add, access & removes of elements in a stack to an array.

<details>

- Access: Does not offer constant-time access to the ith item.
- Add / removes: Does allow constant-time access.

</details>

---

Code a simple stack.

<details>

![](./simpleStack1.png)

![](./simpleStack2.png)

</details>

---

In what type of algorithms might a stack be useful. x2.

<details>

- Recursive algorithms.
- Recursive algorithms implemented iteratively.

</details>

---

## Implementing a Queue

---

What ordering does a queue use?

<details>

- A queue uses FIFO (first-in first-out) ordering.

</details>

---

Detail four queue operations.

<details>

- add(item): Add an item to the end of the list.
- remove(): Remove the first item in the list.
- peek() : Return the top of the queue.
- isEmpty(): Return true if and only if the queue is empty.

</details>

---

Code a simple queue.

<details>

![](./simpleQueue1.png)

![](./simpleQueue2.png)

</details>

---

What are the tricky parts of implementing a queue and should be double checked?

<details>

- The updating of the first and last nodes in a queue.

</details>

---

Name two places where queue are often used.

<details>

- Breadth-first search.
    - Use a queue to store a list of the nodes that we need to process.
    - Each time we process a node, we add it's adjacent nodes to the back of the queue.
    - This allows us to process nodes in the order in which they are viewed.
- Implementing a cache.

</details>

---