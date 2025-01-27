What are files in the computing world? 

-storage : common response

How to interact with files
	-> via the file browser 
The file browser is just a gui 

there is an actual software under the hood to make them real 

Files are not actually storage but *Abstraction*

Abstraction can be summed up as : "A simplification of ideas"

adts - abstract data types

electric car vs interna  combustion engine 
different types of locks -- same sort of thing just different abstraction 

files are much more than storage 

files in the abstract sense dont have names extensions formats... 

how is the abstraction used?
The reason a steering wheel is a steering wheel is just a simplification of the turning process 

Open, Read, Write

Reading bytes of data 
Writing bytes of data 

What other file-like things are on your machine: 
-> A buffer - there actually are like kernel buffers
-> the mouse and keyboard can be framed as files technically 
-> memory -- in the unix world you can write directly to the memory in the form of a file

READ PAPER 

Looking at a file's contents

hexdump -C hello.c 

file here hello.c and using hexdump we can see all of the bytes comprising it 

file tool: makes a guess by looking at the contents of the file to determine its' type

file n.mp3 : C source ascii file 
despite its' name, the contents of the file determine its' type
the file contents knows nothing or stores nothing about its' literal name 

how does the file figure out its' contents

One of the tricks that the file command uses, by convention looking a real mp3 it determines it is a real mp3 due to the file providing *magic bytes* at the beginning of the file
this is not part of the file system 

the os keeps a separate list 

map territory relation 
file names are representations of the file but not actually the file itself, similar to a pointer in C 
gcc will fault if not given real c code, duh cannot be fooled

Masquerading : the file name doesnt say anything about the file
Popular cyber attacks use this by just putting a different type of file contents in a supposed type of file 

How do files get named? 

Obviously we can double click on the file and see the contents we want. 
You have a file store and you can put any type of file you want there. 
A type of file you can put in there is a directory file. 
Every time you make a new file the OS issues that file a unique code number to identify it. 
Special file called a directory file, behaves like a files but can only be written and edited by the OS. 
This is quite literally stored in a text file. Meta data is stored in a text file with the codes of all of the files in the OS. Arbitrarily given numbers. 

Directories are just files. 

We just change the name, keep the same number when using mv. All it does is looks up the file number and then just changes the directory listing 
Inode has its own inode number
recursion 

This is where the tree style file system comes from 

if you save a file do you get a new inode : no 

what if you were to make a copy of a file? New number 
copy basically creates a new file 
when you create a file it just makes a new i node number 
This is just how UNIX is designed 

you can dupe files
how does rm work ?

One thing you could do is remove everything, however most times it removes the number from the inode 
until the file system claims the newly gained space 
basically just like malloc 

when a file is deleted the OS is told that there is new space 

you can make hard links in between directories

hard links 

duping the file by giving the same inode means they are basically the same file despite any names 
exactly like pointers

the inode number determines the contents: the inode is the sequence of bytes

Whats the name of the root file in unix like system: /

the . and the .. files contain the inode numbers of the current and previous giving references 

without giving ls any args it auto uses . which is the current 

there is basically a file that determines each users home dir 

what algorithm could you write to print out all paths 

recursive tree traversal 
skipping the . marking it as seen to avoid the infinite loop of reading pointer to cur and prev 

find does this with no args you can give more params 

there is lots and lots of uses 
files are abstraction file hierachies work because of this 