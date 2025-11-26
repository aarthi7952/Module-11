# 📚 Doubly Linked List: Insert Elements at the End of a Doubly Linked List

This Python program demonstrates the creation and manipulation of a **Doubly Linked List** where elements can be inserted at the **end** of the list. The program also provides a method to traverse the list and display the elements.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List**.
- Allows insertion of elements at the end of the list.
- Provides functionality to traverse the list and display its elements.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` to represent each node in the doubly linked list with attributes:
   - `item` for storing the data of the node.
   - `nref` for storing the reference to the next node.
   - `pref` for storing the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `start_node` to point to the first node of the list.

3. **Step 3:** Define methods in the `DoublyLinkedList` class:
   - `insert_in_emptylist(data)` to insert an element when the list is empty.
   - `insert_at_end(data)` to insert elements at the end of the list.
   - `traverse_list()` to traverse the list and print the elements.

4. **Step 4:** Create an instance of `DoublyLinkedList` and use the `insert_at_end()` method to insert elements into the list.

5. **Step 5:** Use the `traverse_list()` method to print the elements of the list.

---

## 💻 Program
```
class Node:

def init(self, data):

self.item = data

self.nref = None

self.pref = None
class DoublyLinkedList:

def init(self):

self.start_node = None
def insert_in_emptylist(self, data):

if self.start_node is None:

    new_node = Node(data)
    
    self.start_node = new_node

else:
    
    print("list is not empty")
def insert_at_end(self, data):

if self.start_node is None:
    
    new_node = Node(data)
    
    self.start_node = new_node
    
    return

n = self.start_node

while n.nref is not None:

    n = n.nref

new_node = Node(data)

n.nref = new_node

new_node.pref = n
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

new_linked_list.insert_at_end(10)

new_linked_list.insert_at_end(20)

new_linked_list.insert_at_end(30)

new_linked_list.insert_at_end(40)

new_linked_list.traverse_list()
```

## Sample Output
<img width="308" height="188" alt="491483978-314ba4d2-a1ee-4cea-900f-3cfb7922d3e9" src="https://github.com/user-attachments/assets/217efe36-6bcc-461a-9507-6cfa677e95e7" />

## Result
The program is excuted and verified.
# 📝 Doubly Linked List: Search an Element

This Python program demonstrates the implementation of a **Doubly Linked List** where you can insert elements at both the beginning and the end of the list. Additionally, it allows you to search for a specific element in the list.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List** with functions to insert elements at the beginning and the end of the list.
- Implements a search function to check if a given element exists in the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Nodeq` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   - `prev` to store the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `head` to point to the first node.

3. **Step 3:** In the `DoublyLinkedList` class, define methods:
   - `insert_beginning(data)` to insert a node at the beginning.
   - `insert_end(data)` to insert a node at the end.
   - `search(data)` to search for an element in the list.

4. **Step 4:** Create an instance of `DoublyLinkedList`.
   - Insert elements at the beginning and end.
   - Search for specific elements.

---

## 💻 Program
```
class Nodeq:

def init(self, data):

self.data = data 

self.next = None

self.prev = None
class DoublyLinkedList:

def init(self): self.head = None def insert_beginning(self,data): new_node = Nodeq(data)
if(self.head == None): self.head = new_node
return
self.head.prev = new_node
new_node.next = self.head
self.head = new_node

def insert_end(self, new_data): new_node = Nodeq(new_data) if self.head is None: new_node.prev = None self.head = new_node return last = self.head while last.next: last = last.next last.next = new_node new_node.prev = last def search(self,data): temp = self.head while temp: if temp.data==data: break temp = temp.next if temp==None: print("The given data doesnot exist:") return False return True Dllist = DoublyLinkedList()

Dllist.insert_beginning(2)

Dllist.insert_end(0)

Dllist.insert_end(1)

print(Dllist.search(0))

print(Dllist.search(3))
```

## Sample Output
<img width="626" height="164" alt="491484900-547a7dfb-9b45-421c-9f7d-544c7022a665" src="https://github.com/user-attachments/assets/36b44e3e-5c4c-44ba-8269-9456ebb1cc87" />

## Result
The program is excuted and verified.
# 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
```
def init(self, value): self.data = value self.next = None
class LinkedList:

def init(self):

self.head = None
def push(self, new_data):

new_node = Node(new_data)
new_node.next = self.head
self.head = new_node
def printMiddle(self):

temp = self.head
count = 1
while temp is not None:
    if count==3:
        print(temp.data)
    temp = temp.next
    count+=1
llist = LinkedList() for i in range(5): value = int(input()) llist.push(value)

llist.printMiddle()
```

## Sample Input & Output
<img width="379" height="213" alt="491485528-f588d591-5109-477f-b2fb-064b9c0b3ff7" src="https://github.com/user-attachments/assets/5171c286-7d97-477c-8c0b-3f01b7603c76" />

## Result
The program is excuted and verified.
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
# 📝 Singly Linked List: Add Element at the Start

This Python program demonstrates the implementation of a **Singly Linked List** where a new element can be added at the **start** of the list.

---

## 🎯 Aim

To write a Python program that adds a **new element** at the **start** of a singly linked list. The program implements a `push_front` method that inserts an element at the front of the list, followed by a method to print the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   
2. **Step 2:** Define a class `LinkedList` with:
   - `head` to point to the first node.
   
3. **Step 3:** In the `LinkedList` class, define a method `push_front(newElement)`:
   - Create a new node with `newElement`.
   - Set the new node's next pointer to the current head node.
   - Set the head to the new node.

4. **Step 4:** Define a method `PrintList()` to display the list:
   - Print the elements of the list or display "The list is empty." if the list is empty.

5. **Step 5:** Instantiate a `LinkedList` object, `MyList`, and add elements at the start using the `push_front()` method.

6. **Step 6:** Call the `PrintList()` method to display the list.

---

## Program
```

class Node:

def init(self, data):

self.data = data

self.next = None class LinkedList:

def init(self):

self.head = None def push_front(self, newElement):

node = Node(newElement)

node.next = self.head

self.head = node def PrintList(self):

temp = self.head

if(temp != None):

print("The list contains:", end=" ")

while (temp != None):

print(temp.data, end=" ")

temp = temp.next
print()

else:

print("The list is empty.") MyList = LinkedList()

MyList.push_front(10)

MyList.push_front(20)

MyList.push_front(30)

MyList.PrintList()
```
## Sample Output
<img width="542" height="135" alt="491486452-c2431b7f-c24c-4edf-afd7-1766ae042cb6" src="https://github.com/user-attachments/assets/4be5585e-d72c-44d9-a2d4-399539d6f0a6" />

## Result
Thus the progam is excuted and verified.
