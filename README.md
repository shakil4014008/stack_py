# stack_py

````py
normal stack implement
class MyStack:

    def __init__(self):
        self.items = []

    def push(self, item: int) -> None:
        self.items.append(item)

    def pop(self) -> int:
        if not self.empty():
            return self.items.pop()
        else:
            raise IndexError("Stack is empty")

    def top(self) -> int:
        if not self.empty():
            return self.items[-1]
        else:
            raise IndexError("Stack is empty")
    def empty(self) -> bool:
        return len(self.items) == 0    

    def size(self):
        return len(self.items)

=====================================================
Fixed array stack: 

class StackWithCapacity:
    def __init__(self, capacity):
        self.capacity = capacity
        self.items = []

    def push(self, item):
        if self.size() < self.capacity:
            self.items.append(item)
        else:
            raise OverflowError("Stack is full")

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        else:
            raise IndexError("Stack is empty")

    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        else:
            raise IndexError("Stack is empty")

    def is_empty(self):
        return len(self.items) == 0

    def size(self):
        return len(self.items)

# Example usage
stack = StackWithCapacity(3)

stack.push(5)
stack.push(10)
stack.push(15)

print("Stack size:", stack.size())
print("Top element:", stack.peek())

popped_item = stack.pop()
print("Popped:", popped_item)

print("Is stack empty?", stack.is_empty())

----------------implement stack using queue (deque)

class MyStack:
    
    def __init__(self):
        self.queue = collections.deque([])     

    def push(self, x: int) -> None:
        self.queue.append(x)

    def pop(self) -> int:
        return self.queue.pop()
         
    def top(self) -> int:
        return self.queue[len(self.queue)-1]

    def empty(self) -> bool:
        return len(self.queue) == 0
        
        

````
