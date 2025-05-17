### EX: 11.d Doubly Linked List (Insertion and all operation)


### Aim: Type a python program to push elements, insert after and insert before operations in doubly linked list.
### Algorithm:
STEP 1: Create a new node with the given data.
STEP 2:For push, set new node's next to head, update head’s prev to new node (if head exists), then make new node the new head.
STEP 3:For insert after, set new node’s next to previous node’s next, set previous node’s next to new node, and set new node’s prev to previous node.
STEP 4:If the new node’s next is not null, update the next node’s prev to point to the new node.
STEP 5:For insert before, set new node’s prev to next node’s prev, and new node’s next to the next node.
STEP 6:If new node’s prev is not null, update its next to point to new node; otherwise, set head to new node.
STEP 7:Finally, set next node’s prev to new node.

### Program:
```
class Node:
    def __init__(self, data):
        self.data = data 
        self.next = None 
        self.prev = None 

class DoublyLinkedList:
    def __init__(self):
        self.head = None 
        self.tail = None
    def push(self,data):
        new_node=Node(data)
        if self.head is None:
            self.head=new_node
            self.tail=new_node
        else:
            new_node.next=self.head
            self.head.prev=new_node
            self.head=new_node
    def insert_after(self,prev_node,data):
        new_node=Node(data)
        new_node.prev=prev_node
        new_node.next=prev_node.next
        if prev_node.next is not None:
            prev_node.next.prev=new_node
        else:
            self.tail=new_node
        prev_node.next=new_node
    def insert_before(self,next_node,data):
        new_node=Node(data)
        new_node.next=next_node
        new_node.prev=next_node.prev
        if next_node.prev is not None:
            next_node.prev.next=new_node
        else:
            self.heard=new_node
        next_node.prev=new_node
    def display(self):
        current=self.head
        while current is not None:
            print(current.data)
            current=current.next
d=DoublyLinkedList()
d.push(50)
d.push(40)
d.push(30)
d.display()
print("After inserting element at the end")
d.insert_after(d.tail,60)
d.insert_after(d.tail,70)
d.display()


```
### Output:
 
![11B](https://github.com/user-attachments/assets/aeac5d52-3f94-4af7-8bb0-89a056155c55)


 

### Result: Thus, the given program is implemented and executed successfully.
