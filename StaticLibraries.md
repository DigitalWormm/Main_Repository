# Static Libraries in C++
Short Description

## Preliminaries
### What is a Library
Essentially, A library in the Programming world is a collection of source files, header files or programs like .cpp, .cs, or .py depending on the language. These collection of reusable code allow programmers to save time and not have to 'reinvent the wheel'. Great examples of libraries are Spectre in C# (for designing command line interfaces or terminals) and TensorFlow for C++ (for machine learning and AI). There are two types of Libraries. Namely, Dynamic Library and Static Library. 

### Dynamic Library vs Static Library
Dynamic Libraries reside outside the executable file (.exe) while Static Libraries merge the used functions that came from the Library, into the executable (.exe). You can think of this as follows: The executable is the house and the libraries are pets. The cats which are Static libraries stay inside the house while the dogs which are the Dynamic Libraries stay outside of it.

### File Extensions
File extensions are great ways to distinguish whether a library file is static or dynamic.
1. a   - These are _archive files_ which are static libraries most popular in linux operating systems. Though they could also run in windows operating systems.
2. so  - These are _shared objects_ which are dynamic libraries. Similar to the 'archive' file, They are popular in linux.
3. dll - These files are _dyanmic link library_ files which from the name, is a dynamic library. The main distinct difference is that _.dlls_ are designed for the windows operating system and is mostly exclusive to visual studio compilers.
4. lib - Similar to _dll_, _lib_ files are _library_ files which are static. It is the windows counterpart of _a_ or _archive_ files. It is also mostly exclusive to visual studio compilers.

### GNU AR
AR is a tool in GNU ( a collection of developer tools, like a library ) which is mainly used for 

### G++ Review
Short Description

## How to Create a Static Library
Short Description

## How to Link a Static Library
Short Description

```
std::cout << "Hello World";
```

Do you know da wae
- item 1
- item 2
