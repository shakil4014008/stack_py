# stack_py

````py
class Stack:
  def __init__(self, capacity):
    self.nums = []
    self.capacity = capacity
    self.n = 0

  def push(self, value):
    if self.n == self.capacity:
      print("capacity exceeded, cannot push")
      return
    self.nums.append(value)
    self.n += 1
  
  def pop(self):
    if self.n == 0:
      print("stack is empty, cannot pop")
      return
    self.n -= 1
    return self.nums.pop()

stack = Stack(2)
stack.pop()
stack.push(10)
print(stack.nums)
stack.push(100)
print(stack.nums)
stack.push(200)
print(stack.nums)
stack.pop()
print(stack.nums)
stack.pop()
print(stack.nums)
stack.push(450)
print(stack.nums)

````
