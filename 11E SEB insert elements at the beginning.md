11E EX: Function to insert elements at the beginning 

Aim:Type a python function to insert elements at the beginning of the doubly linked list.

Algorithm:
Step 1:Start
Step 2:Define a node structure with data, prev, and next.
Step 3:Create a class for the Doubly Linked List (DLL) with a head pointer.
Step 4:Define a method insert_at_beginning(data):
    Create a new node with the given data.
    Set the next of the new node to current head.
    If the list is not empty, set prev of current head to the new node.
    Set head to the new node.
Step 5:Optional: Define a method to display the list.
Step 6:Call the function and test insertion.
Step 7:End

Program:
```
class Node:
    def __init__(self, data):
        self.item = data
        self.nref = None
        self.pref = None

class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    def insert_in_emptylist(self, data):
        if self.start_node is None:
            new_node = Node(data)
            self.start_node = new_node
        else:
            print("list is not empty")
            
    def insert_at_start(self, data):
        new_node=Node(data)
        if self.start_node is None:
            self.start_node=new_node
        else:
            new_node.nref=self.start_node
            self.start_node.pref=new_node
            self.start_node=new_node
        
    def traverse_list(self):
        if self.start_node is None:
            print("List has no element")
            return
        else:
            n = self.start_node
            while n is not None:
                print(n.item , " ")
                n = n.nref
                
new_linked_list = DoublyLinkedList()
new_linked_list.insert_in_emptylist(40)
new_linked_list.insert_at_start(30)
new_linked_list.insert_at_start(20)
new_linked_list.insert_at_start(10)
new_linked_list.traverse_list()
```
Output:

![11e](https://github.com/user-attachments/assets/5f80c8ec-8164-4b20-b9a8-a5e4550845fe)

Result:
 Thus, the given program is implemented and executed successfully .



