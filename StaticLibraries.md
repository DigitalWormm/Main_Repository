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
AR is a tool in GNU ( a collection of developer tools, like a library ) which I use for creating static Libraries. 

### G++ Review
G++ is a compiler from GNU that compiles C++ code. If you use vscode, then you may have heard code runner. If not then you likely have at least manually compiled your c++ code. A great example of compiling using G++ is the following.
```
g++ Main.cpp -o Main
```
1. g++ invokes or calls the compiler
2. Main.cpp is the program/source code to be compiled
3. -o is a g++ option that specifies the name of the output file
4. Main is the name of the output file. Ends up as 'Main.exe'

## How to Create a Static Library
Short Description

## How to Link a Static Library
When downloading an external library, you must link it to the source code where it is implemented. You can do this by doing the following commands. We will use the library 'curl' as an example. We have Main.cpp as our source code. 

### Main.cpp
```
#include <iostream>
#include "curl/curl.h"

int main(){
  std::cout << "Hello World";
}
```
### Location of Curl Library
Note: The current directory is 'MyProject'. This will be relevant later when we link the library.
```
C:/user/MyProject/src/CURL
```

Now if you try to compile the program, you would get an error. This is because the library curl is not yet linked to it. To do this, you can run the following command.
```
g++ -static Main.cpp -o Main -L./src/CURL/lib -I./src/CURL/include -lcurl
```
1. _-static_ is called here because we are linking the program statically and there are no external dependencies/dynamic libraries involved
2. _-L._ is called here to help the compiler locate the library to be used. Note we want to use _'libcurl.a'_. We do not have to specify the current directory (MyProject), although you could if you want to. Same goes for -I
3. _I._ is called here to locate the header files. Specify the path where the header files are.
4. -l is the library name we want to use. -lcurl expands to libcurl.a

That is it for linking static libraries.
