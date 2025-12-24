# Custom Memory Allocator in C

A **lightweight custom memory allocator** written in C that manages heap memory using a chunk-based linked list approach.

---

## Overview

This project implements a custom memory allocation system as an alternative to the standard `malloc()` and `free()` functions. It demonstrates low-level memory management concepts by organizing the heap into chunks connected via linked lists.

---

## Features

- **Custom allocation**: Allocates memory blocks from the heap
- **Custom deallocation**: Frees memory and returns it to the available pool
- **Chunk-based management**: Uses linked list data structure to track allocated and free memory blocks
- **Educational implementation**: Clean, readable code for learning systems programming concepts

---

## How It Works

The allocator manages memory by:
1. Maintaining a linked list of memory chunks
2. Tracking which chunks are free vs. allocated
3. Coalescing adjacent free chunks to reduce fragmentation
4. Providing `malloc()`-like and `free()`-like interfaces

---

## Building the Project

This project uses CMake for building.
```bash
# Create build directory
mkdir build && cd build

# Generate build files
cmake ..

# Compile
make

# Run
./CustomMemoryAllocatorC
```

---

## Usage Example
```c
// Allocate memory
void* ptr = my_malloc(100);

// Use the memory
// ...

// Free memory
my_free(ptr);
```

---

## Project Structure
```
CustomMemoryAllocatorC/
├── main.c              # Main implementation and test code
├── CMakeLists.txt      # CMake build configuration
└── cmake-build-debug/  # Build output directory
```

---

## Why Build a Custom Allocator?

- **Learn low-level memory management**: Understand how `malloc()` and `free()` work under the hood
- **Performance optimization**: Tailor allocation strategies to specific use cases
- **Systems programming practice**: Gain experience with pointers, linked lists, and heap management
- **Interview preparation**: Common topic in systems programming interviews

---

## Limitations

This is an educational implementation and is not intended for production use. It lacks:
- Thread safety
- Advanced fragmentation prevention
- Alignment guarantees
- Performance optimizations present in production allocators

---

## Contributing

Feel free to fork this repository, experiment with the code, and suggest improvements!

---

## License

Open source - free to use for learning and experimentation.

---

## Author

**Goutham N** ([@GOUTHAM-2002](https://github.com/GOUTHAM-2002))  
📧 goutham3336@gmail.com

---

## Learn More

Interested in memory management? Check out:
- [Doug Lea's malloc implementation](http://g.oswego.edu/dl/html/malloc.html)
- [Understanding glibc malloc](https://sourceware.org/glibc/wiki/MallocInternals)
- [Memory allocation strategies](https://en.wikipedia.org/wiki/Memory_management)
