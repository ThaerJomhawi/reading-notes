# Stacks and Queues

## Stacks:

* Stack: data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

### Stacks follow these concepts:

* **FILO**
***First In Last Out***

the first item added in the stack will be the last item popped out of the stack.

* **LIFO**
***Last In First Out*** 

the last item added to the stack will be the first item popped out of the stack.



**the topmost item is denoted as the `top`. When you push something to the stack, it becomes the new `top`. When you pop something from the stack, you pop the current `top` and set the next top as `top.next`**  


### Common terminology for a stack is:

**1. Pop O(1):**

Popping Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

**2. Peek O(1) :**

conducting a peek, you will only be inspecting the top Node of the stack.

**3. IsEmpty O(1)**

* the pseudocode for isEmpty :

  ` ALGORITHM isEmpty()
    INPUT <-- none
    OUTPUT <-- boolean
    return top = NULL `


## Queues :

terminology for a queue is

1. ***Enqueue*** Nodes or items that are added to the queue.
2. ***Dequeue*** Nodes or items that are removed from the queue.
   > If called when the queue is empty an exception will be raised.
3. ***Front*** This is the front/first Node of the queue.
4. ***Rear*** This is the rear/last Node of the queue.
5. ***Peek*** When you peek you will view the value of the front Node in the queue.
   > If called when the queue is empty an exception will be raised.
6. ***IsEmpty*** returns true when queue is empty otherwise returns false.

**Queues follow these concepts:**

**FIFO** First In First Out.

**LILO** Last In Last Out.