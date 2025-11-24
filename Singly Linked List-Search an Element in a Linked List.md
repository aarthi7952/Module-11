# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
```
class Node:

def init(self, data):

self.data = data

self.next = None
class LinkedList:

def init(self):

self.head = None
def push(self, new_data):

new_node = Node(new_data)

new_node.next = self.head

self.head = new_node
def search(self, x):

current = self.head

while current != None:
    
    if current.data == x:

        return True
    
    current = current.next

return False
llist = LinkedList()

llist.push(10);

llist.push(30);

llist.push(11);

llist.push(21);

llist.push(14);

data = int(input())

if llist.search(data):

print("Yes") else:

print("No")
```
## Sample Output
<img width="320" height="177" alt="491486006-2216e9da-d6b1-43ba-a561-3d96fd500eef" src="https://github.com/user-attachments/assets/da733228-2455-42ed-a73d-ddbe80d609cf" />

## Result
The program is excuted and verified.
