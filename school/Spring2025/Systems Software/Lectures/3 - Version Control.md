Records changes to code
Makes things much easier to fix if you have a record of each changes and who is doing the changes so that you can blame them

Analogy - bank account balance 
Bank just told you have 31 dollars
it is much easier to see that you spent it all on beer 
<-EVIDENCE-> 
Transaction Log makes things easy to understand 

List of transactions removes need for total, just add them all up 

Version control systems work basically the same way

Allows a record to be taken of each change --->  git commit -m "What I did"

use diff (old file, new file) and it shows the difference 

patch tool --> 
				original file                                                       new file 
							diff tool gives us patch file 
			hello.c --> hello.patch
			the patch tool gives us the contents of new hello
			as long as we have a set of differences we can always recover the file 
using the the old new and patch we can take any two and recover the third

-R to undo the patch

patch (original, patch) = new file 
the patch file is exactly what diff outputs

wc -l - show how many lines there are 


version control is a diff based filesystem

diff and patch precede the git tool -- git actually uses - the interface that is presented to you is a series of diffs and patches 



Sections of a git project: 
Working directory -- what you actually working with 
Staging area  -- unique to git, a place where you can collect changes - here are all of the lines of code that i want to add to the diff
Local Repository - hidden directory called .git stores all of the changes and diffs and records

Git stages line by line - however you can also stage the whole file 

running commit will stage the whole file - conceptually you are just logging the changes

add - stages the changes

initial commit- diff area and then a message - conceptually what is stored there is the output of a diff 

blockchain - set up changes with metadata

using git is just adding up a series of diffs - adding them all together you can find the og and new files


multiple changes may fork from the same diff

merge conflicts do suck 

forked - my version is the real one

Commands to change state: 
Emacs - vim -- modify a file 
git add 
git push
git pull 

git status should be used a lot 




changes to be committed means staged 
by default the editor is ez to me VIM my goat 


get used to popping up the editor to make a commit message 

git show will show you the contents 
entire sequence of git log 

important for grading : git remote add submission 