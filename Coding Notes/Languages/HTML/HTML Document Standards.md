Now we learn how to set up an html file :
to begin an html file you have to declare the beginning 
<!DOCTYPE html> 

to begin the structure you need the <html> tags opening and closing 
everything between these tags will be interpreted as html code 


The Head:
the head tag contains the metadata for a webpage
Metadata is information about the page that isn't displayed directly on the page
unlike stuff in the body tag, metadata in the head tag is data about the head itself

Page Titles: 
you can set a title inside of the head tag which is what the browser will display as the page title
The title is what is displayed in the tab on the web browser

Links to other pages:
Html has the ability to link to other pages 
u can add links using the <a> tag
you need to add the attribute href inside of the a tag to actually put the link tho 
and the text in between the opening and closing tags is whats actually shown
href stands for hypertext reference 

Opening links in new window
opening a link and it creating a new window is all thanks to the a tag's target element 
ie: <a href = "bdasodnma.com" target = "_blank">Bear </a > 
this instructs the browser to open the link in a new window 

Linking to a relative page: 
when you want to traverse between pages in the same sort of directory you can just set the href to the file location or name of the relative page ie: <a href="./contact.html">Contact</a> 


Linking at will:
 you can wrap any element with a link tag making it into a link!

Linking inside of the same page: 
	to be able to do this we can give elements id attributes ie: <p id="top">This is the top of the page!</p>  
<h1 id="bottom">This is the bottom! </h1>

the target link is # + the name of the id of the target 

in a list : 
<ul>
 <li><a href = "#link">list item </a>
</ul>

when writing html indent once per generation 

when writing comments do <!-- HI --> 