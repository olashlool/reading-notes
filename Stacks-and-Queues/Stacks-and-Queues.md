# Read 09 : Stacks And Queues

## What is a Stack?

<hr>
> A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
#### Common terminology for a stack includes:

1. Push - Nodes or items that are put into the stack are pushed
2. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
3. Top - this is the top of the stack
4. Peek - When you peed you will view the value of the top Node in the stack. When you attempt to peed an empty stack an exception will be raised
5. IsEmpty - returns true when stack is empty otherwise returns false

#### Stack Ordering
<hr>

- FILO
> First In, Last Out: This means that the first item added in the stack will be the last item popped out of the stack. 
- LIFO
> LIFO - Last In, First Out: This means that the last item added to the stack will be the first item popped out of the stack.

## What is a Queue?
<hr>

>A queue is a linear structure which follows a certain order for performing operations.

#### Common terminology for a Queue is:
<hr>

1. Enqueue - Nodes or items that are added to the queue.
2. Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty and exception will be raised.
3. Front - This is the first Node of the queue
4. Rear - This is the last Node of the queue
5. Peek, you view the value of the front Node
6. IsEmpty

#### Queue Ordering:
<hr>

- FIFO 
> First In, First Out: This means that the first item in the queue will be the first item out of the queue.
- LILO 
> Last In, Last Out: This means that the last item in the queue will be the last item out of the queue.
