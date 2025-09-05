# Memory Allocation and Management in Different Languages


1. Python 🐍

Automatic Memory Management :-

Uses a private heap space managed by the Python Memory Manager.

Developers don’t manually allocate or free memory.


Garbage Collection :- 

Python uses reference counting + generational garbage collector.

Objects with zero references are collected automatically.


Memory Optimizations :-

Small integers & strings are interned for efficiency.

sys.getsizeof() can check object size.



✅ Key takeaway: Python handles memory automatically, but large data structures should be carefully managed. 



2. C++ ⚡

Manual Memory Management :- 

new → allocate memory on heap.

delete → free memory.

Example:

int* ptr = new int(5);
delete ptr;


Stack vs Heap :-

Stack → automatically managed (local variables).

Heap → programmer must allocate/free explicitly.


Issues :-

Dangling pointers, memory leaks, double free.


Smart Pointers :- 

unique_ptr, shared_ptr, weak_ptr manage memory safely.



✅ Key takeaway: Powerful but risky. Proper delete or smart pointers are essential. 



3. Java ☕

Automatic Memory Allocation :-

Objects always created on the heap using new.


Garbage Collection (GC) :-

JVM handles memory cleanup.

Uses generational GC: Young, Old, Permanent generations.


Finalization :-

finalize() method (deprecated in modern Java).


Memory Structure :-

Heap → Objects.

Stack → Method calls, local variables.

Metaspace → Class metadata (replaced PermGen).






