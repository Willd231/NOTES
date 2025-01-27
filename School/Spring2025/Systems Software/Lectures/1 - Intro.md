
What is systems software? 
the bridge between the o s kernel and the apps you use everyday 

what is a kernel - the library that the os uses to interact 
the kernel is the idealized version of the hardware 
all apps are software that live on the top of your machine
os is connective tissue between everything 

Examples of sys software 

Libraries - sdio malloc etc.
Programming toolchains - compilers linkers like gcc and g++ 
programming environments - make, git , gnu toolchain is stuff you use all of the time 

Course goals - 1. use system software, and be conversant in the command line
know  how to use version control do it on nuts and bolts no ide 
projects will be submitted via version control - dogfood style 
understand the file system
be familiar with gnu/Linux dev toolchain 
Linux is the os kernel line 
entire dev through the  command line only
2. be able to build system software
working with file abstraction 
manipulating and creating the abstraction
process management - build bash

build a compiler
working with language processors
gen machine code 
create a compiler that can gen x86 machine code 
make everybody a better programmer :) 

 The tortoise and the hare: they are  both given hard programming assignments 
 this class will consist of hard shit 
 the hare immediately starts coding 
the tortoise starts planning, making tests and planning out everything
the hare finishes really fast
now the real work starts 


the hares code sucks and fails all of the tests 
the tortoise tests each small part individually to make sure each part works
multiple bugs at the same time is hell make sure that \ each small part works
make your own tests and then save those tests 


if you write something super clever, how in the world are you going to be able to discover a system that is even more clever in order to debug


What is a bug? 
It is not that the software isn't doing something right. It is not doing what you want it to do. 
Debugging and programming in general is trying to get the machine to fix the specific problem
The first step is to understand the behavior of the code, use test cases
make the implication match the specification
compartmentalize everything  