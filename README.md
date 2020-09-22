<div align="center">

## Intro to C\+\+ Part 12: Classes


</div>

### Description

C++ is a bunch of small additions to C, and one major addition. This one addition is the object oriented approach. As its name suggests, this deals with objects. This tutorial introduces you to creating objects, or classes.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Alexander of CProgramming\.com](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/alexander-of-cprogramming-com.md)
**Level**          |Intermediate
**User Rating**    |4.5 (58 globes from 13 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Classes/ Frameworks/ OOP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/classes-frameworks-oop__3-31.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/alexander-of-cprogramming-com-intro-to-c-part-12-classes__3-469/archive/master.zip)





### Source Code

<p><font face="Verdana">C++ is a bunch of small additions to C, and one major
addition. This one addition is the object oriented approach. As its&nbsp;name
suggests, this deals with objects. Of course, these are not real-life objects.
Instead, this objects are the essential definitions of real world objects, or
people. Structures are one step away from these objects, they do not possess one
element of them: functions. The definition of these objects are called classes.
The easiest way to think about a class is to imagine a structure that has
functions.</font></p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp;&nbsp; What is this mysterious
structure? Well, it is not only a collection of variables under&nbsp;one
heading, but it is a collection of functions under that same heading. If the
structure is a house, then the functions will be the doors. They usually will be
the only way to modify the variables in this structure, and they are usually the
only to to access the variables in this structure.</font></p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp;&nbsp; From now on, we shall call
these structures with functions classes(I guess Marx would not like C++). The
syntax for these classes is simple. First, you put the keyword 'class' then the
name of the class. Our example will use the name computer. Then you put the
different variables you want the class to hold. In our example, there will be
only one, processor speed.&nbsp; However, before putting down the different
variable, it is necessary to put the degree of restriction on the variable.
There are three levels of restriction. The first is public, the second
protected, and the third private. For now, all you need to know is that the
public specifier allows any part of the program, including what is not part of
the class, access the variables specified as public. The private specifier
allows only the functions of the class that owns (not a technical term) the
variable to access that variable.</font></p>
<p><font face="Verdana">#include &lt;iostream.h&gt;</font></p>
<p><font face="Verdana">class computer //Standard way of defining the class</font></p>
<p><font face="Verdana">{</font></p>
<p><font face="Verdana">private: //This means that all the variables under this,
until a new type of restriction is</font></p>
<p><font face="Verdana">//placed, will only be accessible to functions that are
part of this class.</font></p>
<p><font face="Verdana">//NOTE: That is a colon, NOT a semicolon...</font></p>
<p><font face="Verdana">int processorspeed;</font></p>
<p><font face="Verdana">public: //This means that all of the functions below
this(and variables, if there were any)</font></p>
<p><font face="Verdana">//are accessible to the rest of the program.</font></p>
<p><font face="Verdana">//NOTE: That is a colon, NOT a semicolon...</font></p>
<p><font face="Verdana">void setspeed(int p); //These two functions will be
defined outside the class</font></p>
<p><font face="Verdana">int readspeed();</font></p>
<p><font face="Verdana">}; //Don't forget the trailing semi-colon</font></p>
<p><font face="Verdana">void computer::setspeed(int p) //To define a function
outside put the name of the function</font></p>
<p><font face="Verdana">//after the return type and then two colons, and then
the name</font></p>
<p><font face="Verdana">//of the function.</font></p>
<p><font face="Verdana">{</font></p>
<p><font face="Verdana">processorspeed = p;</font></p>
<p><font face="Verdana">}</font></p>
<p><font face="Verdana">int computer::readspeed() //The two colons simply tell
the compiler that the function is part</font></p>
<p><font face="Verdana">//of the class</font></p>
<p><font face="Verdana">{</font></p>
<p><font face="Verdana">return processorspeed;</font></p>
<p><font face="Verdana">}</font></p>
<p><font face="Verdana">void main()</font></p>
<p><font face="Verdana">{</font></p>
<p><font face="Verdana">computer compute; //To create an 'instance' of the
function, simply treat it like you would<br>
//a structure. (An instance is simply when you create an actual object<br>
//from the class, as opposed to having the definition of the class)<br>
</font></p>
<p><font face="Verdana">compute.setspeed(100); //To call functions in the class,
you put the name of the instance,<br>
//and then the function name.</font></p>
<p><font face="Verdana">cout&lt;&lt;compute.readspeed(); //See above note.</font></p>
<p><font face="Verdana">}</font></p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp;&nbsp; As you can see, this is a
rather simple concept. However, it is very powerful. It makes it easy to prevent
variables that are contained(or owned) by the class being overwritten
accidentally. It also allows a totally different way of viewing programming.
However, I want to end this tutorial as an introduction. I am going to be
writing more tutorials on classes, which will go into more details on classes.</font></p>

