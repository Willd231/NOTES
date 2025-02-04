The process abstraction - a process is a running program 

Difference between a program and a running program 
what is a program? : A set of instructions 
where is your program stored? In file on disk
What kind of instructions does your file program have? Machine code
What makes a program a running program? It is on the processor/cpu 
Your program is just a set of instructions can be anywhere, a running program is running on cpu 

How is it possible to have so many processes running at the same time ? You share the time of the processor - time splicing - illusion of what you are doing to be the only thing happening 
Processors save the state of the cpu 
process ids for all of the processes 
saves current working directory
saves pointer to its memory 
file descriptors 
Multithreading works by having multiple processes inside of the process 

in the unix world and the style of making system calls is dumb 
the only way that you can make a new process is by duping your current process the exec replaces the program in your current process with a new program 

once you fork, there is two of your same program, if you call exec by itself, the hello program ceases to run, the exec doesnt do any it just swaps the current 

what exec does is takes the program code of the process layout and then replaces it with a different program, fork creates an exact dupe 

copy with fork, replace with exec 

threads and processes under the hood are not very different 
the return value of fork tells you what process you are on 
a process is a running program, just like with files where the kernel maintains on disk the inodes it also stores the running processes 

commonly fork and exec are paired, call fork to create a new process and then exec to replace that process with what you want 
to you the dev, it appears all of these processes are separate , it would be very expensive to access all of the memory, conceptually its copying the whole file, similar to mv 

process abstraction provides this mem isolation 
when you swap between processes the cache saved there becomes inefficient 


the process is really just the state of the machine and the processes have the program counter which stores the state of the machine and the kernel stores all of the info allowing the cpu to switch seamlessly allowing for the abstraction and illusion of only one thing running at a time 

the new process is not called something different 
you end up with a process tree 
pstree 
what is the root of the process tree, the initial process has changed over the years but when the kernel boots up it creates an init 
newer systems have a system D for daemon 
these are just processes that run in the background 
The last thing it does on boot is create the init process 
it will open/create the ssh daemon
 we have this systemd process that forks and in the new process that it creates it calls exec and when it receives the login, it execs a shell program for you 
 there is actually  a file that tells the ssh daemon what program to run when the user logs in 

everything derives from a fork from systemd 
there is a program called ps for processes 
like files each process is given a unique identity 

a lot of processes are generally sitting and waiting for something 

fork bombs 
i wonder if eustis has protections 

ps - process 
ps aux - all processes 
ps  tree 
htop - real time mem usage 
you can stop processes using kill from the command line 
call program and then the bash program is running fork and exec using the name of the program 
the shell by convention has a var $PATH that contains the path 
if you zero out the path var you cant run ls 
there is a file that contains a default set of path
there is a nice thing called which will display the path 
cd doesnt have a path 
so bash itself when you call cd it changes bash's own cd  
how would you run a program called cd, ./c

where does printf's output go
standardoutput
where does standardout go 
nowhere 
every process when it is created is given 3 files when it is created 
stdin 
stdout
stderr 
you dont have to specify these because it is automatically assumed that all files need these 
whoever called bash sets up its own standard io 

ultimately systemd is what creates its standard io for its children 

sshd is giving bash its standardio on the terminal 
the ls program does not care where its going just say printf and the system that creates that process will determine where that goes 

by assuming that all program has standardio at one particular place allows you as the programmer to write anywhere and not have to worry about creating fileio 
the convention is just that the first three openfiles are the standard io out and error 
why standard io - remove hardware limitations 
why separate standardout and error -- this is just a convention 
you want to see the error aside from the output, it is very useful to separate these two 

where does standard io go
echo is a program that takes command line args and takes them to stdardio 
you can specify where you want cat to write, the terminal can act like stdio 
this is exemplified through the usage of cat on a file 
stdin < 
out > 
err 2> 
double arrow  = append 

redirection is good for saving outputs to files 
every process is born with out in and err 
