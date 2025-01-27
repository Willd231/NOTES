How to determine which elements get the style?
With a selector of course! 

The colon inside of the curly brackets must be touching the initial specifier 
Type selectors are basically just like elements inside of the html file 

using * works to select every element
its called the universal selector
using the border keyword in css allows for obviously a border to be around things u can specify color and width in px or rem

Selecting elements using css is very inefficient especially if you dont want everything to look the same
to remedy this we can simply give elements in the html file attributes and then access those by putting a  .  in front of their name 

elements can also have more than one attribute which can fall under different selectors

we can also give elements custom ids to give them a unique style by accessing only that id in css

<h1 id = 'cool-title'></h1>

#cool-title{

}

html is really weird about the way you use colons and equal signs 
they must be touching the first thing in the equation to be valid!!!

using css you can target attributes specifically like href, src, and class 

to do this you use the square brackets around the attribute and then the normal {;}


Pseudo class :
:focus, :visited, :disabled, and :active are all examples of pseudo classes 

you can attach pseudoclasses to selectors 
ie: p:hover{
background-color:lime; 
}

css also supports selecting other elements that are nested within other elements, these are called descendants 

when doing descendants, write the class first, and then write the element 
you dont need ids or classes to do descendants however, you can also nest elements from html files if they are inside of each other like with lists 

so when you have a selector for lists and the selector is nested you can deem this as much more specific, adding a selector for the element inside of the nest by itself gets trumped by the nested one because css has a preference for more specific selectors 

its also possible to add selectors to multiple elements at once 
you can do this by adding a comma in between the two ie :

h1, 
.menu{
font-family: Georgia;
}