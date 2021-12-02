    class Queue:
    def __init__(self):
        self.q=[]
        self.front=0
        self.rear=-1
    def enqueue(self,item):
        self.q.insert(0,item)
        
    def dequeue(self):
        self.q.pop()
        
    def size(self):
        return len(self.q)
        
    def isEmpty(self):
        return self.q==[]
        
    def peek(self):
        if self.isEmpty():
            print("Queue is empty")
            exit(-1)
        return self.q[self.rear]
q=Queue()
n=int(input("Enter size of the queue:"))
print("Enter the elements of the queue")
for i in range(0,n):
    x=int(input())
    q.enqueue(x)
print("printing the queue:")
while q.size()>0:
    print(q.peek())
    q.dequeue()
    
