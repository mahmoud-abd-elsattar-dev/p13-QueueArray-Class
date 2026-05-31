# 📋 clsMyQueueArr — Array-Based Queue Library

A generic C++ queue implementation built on top of `clsDynamicArray`, supporting standard FIFO queue operations alongside extended utilities like reverse, insert at front/back, and index-based access.

---

## 📖 Overview

`clsMyQueueArr` is a reusable template-based C++ class that implements a queue (FIFO) data structure using `clsDynamicArray` as its underlying storage. It mirrors the interface of `clsMyQueue` but uses a dynamic array instead of a doubly linked list, making it a great comparison between the two underlying data structures.

---

## ✨ Features

- **Standard Queue Operations**: Push, Pop, Front, Back, Size, IsEmpty, Clear
- **Reverse**: Reverse the queue in-place
- **Insert at Front / Back**: Flexible insertion beyond standard enqueue
- **Index-Based Access**: Get or update an item by index
- **Insert After Index**: Insert a new item after a specific position
- **Generic Type Support**: Works with any data type via C++ templates

---

## 🚀 How to Use

```cpp
#include "clsMyQueueArr.h"
```

### Basic Usage
```cpp
clsMyQueueArr<int> queue;

queue.Push(10);
queue.Push(20);
queue.Push(30);

queue.Print();          // 10 20 30
cout << queue.Front();  // 10
cout << queue.Back();   // 30
cout << queue.Size();   // 3

queue.Pop();
queue.Print();          // 20 30
```

### Extended Operations
```cpp
queue.InsertAtFront(5);    // 5 20 30
queue.InsertAtBack(99);    // 5 20 30 99
queue.InsertAfter(1, 50);  // 5 20 50 30 99
queue.UpdateItem(0, 77);   // 77 20 50 30 99
queue.Reverse();
queue.Print();
```

---

## 🧠 Concepts Used

- **Templates** — Generic class supporting any data type via `template <class T>`
- **OOP** — Encapsulation of queue behavior inside a class
- **Composition** — Uses `clsDynamicArray` as internal storage
- **FIFO Design** — Push adds to the back, Pop removes from the front
- **Delegation** — All methods delegate directly to the underlying dynamic array
- **Inheritance-Ready** — `protected` member `_MyList` allows subclasses to extend behavior

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `Push()` | Adds an item to the back of the queue |
| `Pop()` | Removes the front item from the queue |
| `Front()` | Returns the value at the front of the queue |
| `Back()` | Returns the value at the back of the queue |
| `Size()` | Returns the number of items in the queue |
| `IsEmpty()` | Returns true if the queue has no items |
| `Clear()` | Removes all items from the queue |
| `Reverse()` | Reverses the queue in-place |
| `InsertAtFront()` | Inserts a new item at the front |
| `InsertAtBack()` | Inserts a new item at the back |
| `InsertAfter()` | Inserts a new item after a given index |
| `GetItem()` | Returns the value at a given index |
| `UpdateItem()` | Updates the value at a given index |
| `Print()` | Prints all queue items from front to back |

---

## 🔗 Dependency

This class depends on [`clsDynamicArray`](../clsDynamicArray/) as its underlying data structure.

---

## 📄 License

This project is open source and free to use for educational purposes.

---

## 👤 Author

👤 **Mahmoud Abd El-Sattar**  
📧 mahmoud.abdelsattar.dev@gmail.com  
💼 [linkedin.com/in/mahmoud-abd-el-sattar](https://www.linkedin.com/in/mahmoud-abd-el-sattar-1b227522a)
