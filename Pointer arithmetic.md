---
Theme:
  - "[[C++]]"
---

#### Linear Memory Representation

| Address | Value (1 byte) |
|---------|---------------|
| 0x0000  | ... |
| ...     | ... |
| 0x1000  | 1 |
| 0x1001  | 2 |
| 0x1002  | 3 |
| 0x1003  | 4 |
| ...     | ... |
| 0xffffffffff | ... 

```C++
// Just stores an arbitrary address
void* addr = (void*)0x1000;

// If a pointer doesn’t point anywhere,
// you should use nullptr
void* invalid = nullptr;

// The size of a pointer (here 4) is the number
// of bytes required to store an address (32-bit build)
size_t size = sizeof(addr);  // size == 4

// Now we tell the compiler how to
// interpret the memory the pointer refers to
char* charPtr = (char*)0x1000;

// Dereferencing — retrieving the value located
// at the specified address
char c = *charPtr;           // c == 1

// & — address-of operator; charPtrPtr now holds
// the address of charPtr
char** charPtrPtr = &charPtr;

int* intPtr = (int*)addr;
int  i      = *intPtr;       // i == 0x04030201 (little-endian)

// Pointer arithmetic in elements
int* i1 = intPtr;
int* i2 = i1 + 2;

ptrdiff_t d1 = i2 - i1;      // d1 == 2

// Pointer arithmetic in bytes
char* c1 = (char*)i1;
char* c2 = (char*)i2;

ptrdiff_t d2 = c2 - c1;      // d2 == 8
```