Important but overlooked part of software development
How to build a C program? 

By using gcc. 

What if there are two files, how to compile both of them together? 

by providing gcc with two inputs and one output executable

What if there are 30,000 files?

You would have to provide 30,000 source files.  

We don't do this. 

When you make a single line change you would have to recompile. 

We will use separate compilation. 

Divide program into separate files and then use a linker. 


main.c         square.c           exponent.c

gcc -c            gcc -c             gcc -c

using -c gives us object files for each

main.o        square.o           exponent.o 


	        id


 libxz - vulnerability 
big attack 
they imported the backdoor using libxz 
in the build process the modifications got into the source code 
they attempted to ssh  



makefiles 

target  recipe 


when using make u can insert wildcards to build multiple at once 

phony targets

you can provide phony targets to execute recipes without making new build files 

you can write bash code inside of makefiles in order to automate