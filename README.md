

# TODO _list_



# Class 1 

        * Herramientas de trabajo,
         Sublime text 3 (instalar, configurar, ...)
         Command line
         Markdown
         Git (github)




#Github

https://try.github.io

# Git Command-line
Git cheat sheet: http://files.zeroturnaround.com/pdf/zt_git_cheat_sheet.pdf

pwd outputs the name of the current working directory.
ls lists all files and directories in the working directory.
cd switches you into the directory you specify.
mkdir creates a new directory in the working directory.
touch creates a new file inside the working directory.
ls -a lists all contents of a directory, including hidden files and directories
ls -l lists all contents in long format
ls -t orders files and directories by the time they were last modified
Multiple options can be used together, like ls -alt
cp copies files
mv moves and renames files
rm removes files
rm -r removes directories

*Git commands

git init
git add
git commit -a
git commit -m "Initial commit"
git status
git log
git checkout
git checkout head
git diff
Remote repositories
Connecting a Remote Repository: git remote add + repository name + url
git clone + url
Uploading data to a Remote Repository: git push
Integrating remote changes: git pull => git fetch + git merge
git reset => remove from the staging area
git checkout master => get back to the “current” state (latest commit) of the project


# Class 2

*Javascript Basics

Clear Ideas, JS History, ECMAScript
Variables, Data Types and Operators
Conditions and Loops

*Javascript Functions

Funciones
Estructura y Parametros
Funciones pre-definidas
Scope de las funciones
Funciones Callback
Closures [1] [2] [3]
Closures Examples

*Pre-defined functions

parseInt()
parseFloat()
isNaN()
isFinite()
encodeURI()
decodeURI()
encodeURIComponent()
decodeURIComponent()
eval()

*Functions Scope

In Javascript variables are defined in the function scope (and not in the block scope as it happen in other languages)

Global variables are those defined out of any function
Local variables are those defined inside of a function

*Callback Functions

Functions in Javascript are data (values), which means they can be assigned to variables in the same way we do with other values (and manage them as variables)

function f(){ return 1; }
var f = function(){ return 1; }

Closures

If we define a function n() inside of another function f() , n() will have access to all the variables in its scope and its father's scope. This is what is called scope chain

var a = 1;
function f(){
  var b = 1;
  function n() {
    var c = 3;
  }
}
http://stackoverflow.com/questions/1484143/scope-­‐chain-­‐in-­‐javascript
http://www.digital-­‐web.com/articles/scope_in_javascript/
http://odetocode.com/Blogs/scott/archive/2007/07/10/closure-­‐on-­‐javascript-­‐closures.aspx
http://www.smashingmagazine.com/2009/08/01/what-­‐you-­‐need-­‐to-­‐know-­‐about-­‐javascript-­‐scope/

Functions have what is called as lexical scope which means they create theis scope (which variables can they access) when they are defined, not when they are executed

https://developer.mozilla.org/en/JavaScript/Guide/Closures
http://stackoverflow.com/questions/1047454/what-­‐is-­‐lexical-­‐scope
http://ayende.com/Blog/archive/2007/12/13/Javascript-­‐lexical-­‐scopes-­‐and-­‐what-­‐your-­‐momma-­‐thought-­‐you-­‐about.aspx

A closure is created when a function maintains a link with the scope of the father, even after the parent function has finished

http://stackoverflow.com/questions/111102/how-­‐do-­‐javascript-­‐closures-­‐work
http://jibbering.com/faq/notes/closures/
http://www.bennadel.com/blog/1482-­‐A-­‐Graphical-­‐Explanation-­‐Of-‐Javascript-­‐Closures-­‐In-­‐A-­‐jQuery-­‐Context.htm

*Javascript Objects

Arrays and Objects (Constructors)
Global Objects (Object, Function, Array, Number, Boolean, Math and Date)

*Javascript Challenge 1
"link" mis ejercicios...


# Class 3

*Javascript Arrays

Arrays
Array as an Object
Array basic methods
Functional programming w/ array higher order functions

*Js array methods

-concat()    
Joins two or more arrays, and returns a copy of the joined arrays
-every()    
Checks if every element in an array pass a test
-fill()    
Fill the elements in an array with a static value
-filter()    
Creates a new array with every element in an array that pass a test
-find()    
Returns the value of the first element in an array that pass a test
-forEach()    
Calls a function for each array element
-indexOf()    
Search the array for an element and returns its position
-join()    
Joins all elements of an array into a string
-lastIndexOf()    
Search the array for an element, starting at the end, and returns its position
-map()    
Creates a new array with the result of calling a function for each array element
-pop()    
Removes the last element of an array, and returns that element
-push()    
Adds new elements to the end of an array, and returns the new length
-reduce()    
Reduce the values of an array to a single value (going left-to-right)
-reverse()    
Reverses the order of the elements in an array
-shift()    
Removes the first element of an array, and returns that element
-slice()    
Selects a part of an array, and returns the new array
-some()    
Checks if any of the elements in an array pass a test
-splice()    
Adds/Removes elements from an array
-toString()    
Converts an array to a string, and returns the result
-unshift()    
Adds new elements to the beginning of an array, and returns the new length
-valueOf()    
Returns the primitive value of an array


*Javascript Objects

Object.keys(obj)

Constructor Functions
function Human(name, surname, weight, height, gender) {
    this.name = name;
    this.surname = surname;
    this.age = 0;
    this.height = height;
    this.weight = weight;
    this.gender = gender;
    this.eat = function(food) { console.log('eating ' + food); };
    this.sleep = function() { console.log('Zzzzz'); };
}

 var Pedro = new Human ('Pedro', 'Jimenez', 3.2, 0.4, 'male')
 console.log(Pedro)
Human {name: "Pedro", surname: "Jimenez", age: 0, height: 0.4, weight: 3.2, eat: function (food), sleep: function ()}

 Pedro.gender
"male"

 Pedro instanceof Object
true
 Pedro instanceof Human
true

Prototypes
function Programmer(workingCompany) {
    this.workingCompany = workingCompany;
    this.program = function(language) { console.log('tktkt tktkt tktkt ' + language); };
}
Programmer.prototype = new Human();

 var Juan = new Programmer ('Skylab')
 Juan
Programmer {workingCompany: "Skylab", program: function}

 Juan.workingCompany
"Skylab"
 Juan.gender
undefined
 Juan instanceof Human
true
 Juan instanceof Programmer
true
Programmer object inherits the properties of the Human object even though it has undefined value

"link" mis ejercicios...

# Class 4

Regular Expressions.


PATTERN         NOTES
/b[aeiou]t/     Matches "bat", "bet", "bit", "bot" and "but"
                Also matches "cricket bat", "bitter lemon"

PATTERN         NOTES
/[0-9a-f]*/     Will match hex
/[0-9a-zA-Z]/   Upper and lower case are distinct; this matches alphanumeric strings
/./ The dot '.' matches any character
/\./            If you actually want to match a dot, escape it

PATTERN         NOTES
/b[aeiou]+t/    Matches "bat" and "bit" etc, but also "boot" and "boat"

PATTERN         NOTES
/^b[aeiou]t/    Will match "battering ram" but not "cricket bat"

*Flags:

g: global
i: ignoreCase
m: multiline

Methods:

test(): Returns true if it finds something and false if it doesn't    
exec(): Return an array of string that match the pattern    
match(): Return an array of occurrences    
search(): Return the position of the first occurrence    
replace(): Allow us to replace the found string by another string    
split(): Accepts a regular expression to split a string in elements of an array    


function fun() {
    this.hello = 'hello!';
}

 fun();
 window.hello;
"hello!"

 var obj = {};
 fun.call(obj);


function fun(name) {
    this.hello = 'hello ' + name + '!';
}

 var obj = {};
 fun.call(obj);
 obj.hello
"hello undefined!"

 fun.call(obj, 'Didac')
"hello Didac!"

 fun ('peter')
 window.hello
"hello peter!"
function Animal(species, name) {
    this.setSpecies(species);
    this.setName(name);
}
Animal.prototype.setSpecies = function(species) {
    this._species = species;
};
Animal.prototype.getSpecies = function() {
    return this._species;
};
Animal.prototype.setName = function(name) {
    this._name = name;
};
Animal.prototype.getName = function() {
    return this._name;
};
Animal.prototype.heal = function() {
    console.log('healing...');
};
Animal.prototype.eat = function () {
    console.log('eating...');
};
Animal.prototype.pee = function () {
    console.log('pssssing....');
};
Animal.prototype.poo = function() {
    console.log('poofffffff....');
};
Animal.prototype.sleep = function() {
    console.log('Zzzz');
};


function Tiger(name, speed) {
    Animal.call(this, 'tiger', name);
    this.setSpeed(speed);
}

Tiger.prototype = new Animal();
Tiger.prototype.setSpeed = function(speed) {
    this._speed = speed;
};
Tiger.prototype.getSpeed = function() {
    return this._speed;
};
Array.prototype.random = function random() {
    return this[Math.floor(Math.random() * this.length)];
}

function randomArg() {
     return Array.prototype.random.call(arguments);
}

*Closures
// Buen ejemplo !! 

function SafeBox(thing) {
    var secret = thing;
    return function (pass) {
        if (pass === 'dame un besito') {
            return secret
        }
        return 'no'
    }
}

 var caja = new SafeBox('me gusta jugar al futbol en pel...')
 caja ('pass')
"no"
 caja('dame un besito')
"me gusta jugar al futbol en pel..."

 *Javascript Challenge 1** Extra

"link" mis ejercicios..

# Class 5

arr = [1,2,3,4,5];

Math.max(...arr);

Return arr // seria 5;



# Class 6


- HTML5 -
https://www.w3.org/TR/html401/struct/global.html

Clear Ideas

The Three Layers of Web Design
CSS Zen Garden (layer separation example)
Structure of an HTML document [1] [2]
Review of basic HTML tags [1]

demo web - http://www.csszengarden.com/

- SEO -

Search engine optimization  

Search engine optimization (SEO) is the process of affecting the visibility of a website or a web page in a web search engine's unpaid results—often referred to as "natural", "organic", or "earned" results. In general, the earlier (or higher ranked on the search results page), and more frequently a site appears in the search results list, the more visitors it will receive from the search engine's users; these visitors can then be converted into customers.[1] SEO may target different kinds of search, including image search, video search, academic search,[2] news search, and industry-specific vertical search engines. SEO differs from local search engine optimization in that the latter is focused on optimizing a business' online presence so that its web pages will be displayed by search engines when a user enters a local search for its products or services. The former instead is more focused on national searches.

HTML basic Body

Here's an example of a simple HTML document:

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>My first HTML document</TITLE>
   </HEAD>
   <BODY>
      <P>Hello world!
   </BODY>
</HTML>


The HEAD element

!-- %head.misc; defined earlier on as "SCRIPT|STYLE|META|LINK|OBJECT" -->
!ENTITY % head.content "TITLE & BASE?">
!ELEMENT HEAD O O (%head.content;) +(%head.misc;) -- document head -->
!ATTLIST HEAD
  %i18n;                               -- lang, dir --
  profile     %URI;          #IMPLIED  -- named dictionary of meta info --
  >


  The TITLE element

    !-- The TITLE element is not considered part of the flow of text.
       It should be displayed, for example as the page header or
       window title. Exactly one title is required per document.
    -->
    !ELEMENT TITLE - - (#PCDATA) -(%head.misc;) -- document title -->
    !ATTLIST TITLE %i18n>


    
 *The BODY element

!ELEMENT BODY O O (%block;|SCRIPT)+ +(INS|DEL) -- document body -->
!ATTLIST BODY
  %attrs;                              -- %coreattrs, %i18n, %events --
  onload          %Script;   #IMPLIED  -- the document has been loaded --
  onunload        %Script;   #IMPLIED  -- the document has been removed --




 
 Using external (linked) style sheets gives you the flexibility to change the presentation without revising the source HTML document:

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>A study of population dynamics</TITLE>
 <LINK rel="stylesheet" type="text/css" href="smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

 Element identifiers: the id and class attributes.

 Attribute definitions

id = name [CS]
This attribute assigns a name to an element. This name must be unique in a document.
class = cdata-list [CS]
This attribute assigns a class name or set of class names to an element. Any number of elements may be assigned the same class name or names. Multiple class names must be separated by white space characters.
The id attribute assigns a unique identifier to an element (which may be verified by an SGML parser). For example, the following paragraphs are distinguished by their id values:
<P id="myparagraph"> This is a uniquely named paragraph.</P>
<P id="yourparagraph"> This is also a uniquely named paragraph.</P>
The id attribute has several roles in HTML:

As a style sheet selector.
As a target anchor for hypertext links.
As a means to reference a particular element from a script.
As the name of a declared OBJECT element.
For general purpose processing by user agents (e.g. for identifying fields when extracting data from HTML pages into a database, translating HTML documents into other formats, etc.).
The class attribute, on the other hand, assigns one or more class names to an element; the element may be said to belong to these classes. A class name may be shared by several element instances. The class attribute has several roles in HTML:

As a style sheet selector (when an author wishes to assign style information to a set of elements).
For general purpose processing by user agents.
In the following example, the SPAN element is used in conjunction with the id and class attributes to markup document messages. Messages appear in both English and French versions.

<!-- English messages -->
<P><SPAN id="msg1" class="info" lang="en">Variable declared twice</SPAN>
<P><SPAN id="msg2" class="warning" lang="en">Undeclared variable</SPAN>
<P><SPAN id="msg3" class="error" lang="en">Bad syntax for variable name</SPAN>
<!-- French messages -->
<P><SPAN id="msg1" class="info" lang="fr">Variable d&eacute;clar&eacute;e deux fois</SPAN>
<P><SPAN id="msg2" class="warning" lang="fr">Variable ind&eacute;finie</SPAN>
<P><SPAN id="msg3" class="error" lang="fr">Erreur de syntaxe pour variable</SPAN>


Block-level and inline elements

Certain HTML elements that may appear in BODY are said to be "block-level" while others are "inline" (also known as "text level"). The distinction is founded on several notions:

Grouping elements: the DIV and SPAN elements

!ELEMENT DIV - - (%flow;)*            -- generic language/style container -->
!ATTLIST DIV
  %attrs;                              -- %coreattrs, %i18n, %events --
  
!ELEMENT SPAN - - (%inline;)*         -- generic language/style container -->
!ATTLIST SPAN
  %attrs;                              -- %coreattrs, %i18n, %events --
  

*Start tag: required, End tag: required

Attributes defined elsewhere

id, class (document-wide identifiers)
lang (language information), dir (text direction)
title (element title)
style (inline style information)
align (alignment)
onclick, ondblclick, onmousedown, onmouseup, onmouseover, onmousemove, onmouseout, onkeypress, onkeydown, onkeyup (intrinsic events)

Headings: The H1, H2, H3, H4, H5, H6 elements

!ENTITY % heading "H1|H2|H3|H4|H5|H6">
!--
  There are six levels of headings from H1 (the most important)
  to H6 (the least important).
-->

!ELEMENT (%heading;)  - - (%inline;)* -- heading -->
!ATTLIST (%heading;)
  %attrs;                              -- %coreattrs, %i18n, %events --


Basic tags. HTML

https://www.lehigh.edu/~inwww/old_seminar/tagreview.html

The fundamental points:

Web documents are ordinary text files (ASCII) that:
Contain tags, which are used to "mark-up" text.
Are named with a ".html" extension.
Are placed in a "www-data" directory within AFS public space.
Tags are just text with a special format:
Each individual tag begins with the character "<"
Each individual tag ends with the character ">"
A tag may contain keywords, the first of which is the name of the tag. 
e.g., <XYZ KEY=VALUE> would be called an "XYZ-tag."
Most tags come in pairs: an opening tag, and a closing tag, which has the same name preceded by a "/".
The text between the two tags is affected by them.
The tags we have discussed are:

<HTML> First tag in a document (unpaired).
<HEAD> Marks the head section (paired).
<BODY> Marks the body section (paired).
<TITLE> Title (goes in head section) (paired).
<P> Paragraph break (unpaired).
<BR> Line break (unpaired).
<HR> Horizontal rule (line) (unpaired).
<PRE> Preformatted text (paired).
<EM> Emphasis (usually italics) (paired).
<STRONG> Stronger emphasis (paired).
<B> Bold (text attribute) (paired).
<I> Italics (text attribute) (paired).
<H1> Level 1 (e.g., document) heading (paired).
<H2> Level 2 (e.g., part) heading (paired).
<H3> Level 3 (e.g., chapter) heading (paired).
<H4> Level 4 (e.g., section) heading (paired).
<H5> Level 5 (e.g., subsection) heading (paired).
<H6> Level 6 (e.g., paragraph) heading (paired).


Document Outline in HTML5

In HTML5 the outlining algorithm has been enhanced by new sectioning elements, namely:

<section></section> for sections grouped around a specific theme
<article></article> for complete or self-contained compositions such as a blog post or a widget
<nav></nav> for navigation blocks
<aside></aside> for complementary content such as sidebars.
There’s a fifth sectioning element in HTML5, but it’s not new, it’s the <body></body> tag. The <header></header> and <footer></footer> tags are also new, but they don’t generate new sections in a document, they divide up the content inside sections. 

HTML5 offers new elements for better document structure:

Tag Description
Defines an article in a document
Defines content aside from the page content
Isolates a part of text that might be formatted in a different direction from other text outside it
Defines additional details that the user can view or hide
Defines a dialog box or window
Defines a caption for a element
Defines self-contained content
Defines a footer for a document or section
Defines a header for a document or section
 Defines the main content of a document
 Defines marked/highlighted text
men Defines a command/menu item that the user can invoke from a popup menuDefines a scalar measurement within a known range (a gauge)
Defines navigation links
pro Represents the progress of a task
Defines what to show in browsers that do not support ruby annotations
Defines an explanation/pronunciation of characters (for East Asian typography)
Defines a ruby annotation (for East Asian typography)
Defines a section in a document
summDefines a visible heading for aelement
Defines a date/time
 Defines a possible line-break

html5-form-validation
http://www.the-art-of-web.com/html/html5-form-validation/


# Class 7

CSS3 Basics & Selectors

class, id,..

Example Classification  Explanation
h1 --> Type Selector Selects an element by it’s type
.tagline --> Class Selector  Selects an element by the class attribute value, which may be reused multiple times per page
#intro --> ID Selector Selects an element by the ID attribute value, which is unique and to only be used once per page


Child Selectors Overview

Example Classification  Explanation
article h2 --> Descendant Selector Selects an element that resides anywhere within an identified ancestor element
article > p --> Direct Child Selector Selects an element that resides immediately inside an identified parent element

Sibling Selectors Overview

Example Classification  Explanation
h2 ~ p --> General Sibling Selector  Selects an element that follows anywhere after the prior element, in which both elements share the same parent
h2 + p --> Adjacent Sibling Selector Selects an element that follows directly after the prior element, in which both elements share the same parent

Attribute Selectors Overview

Example Classification  Explanation
a[target] Attribute Present Selector  Selects an element if the given attribute is present

a[href="http://google.com/"]  Attribute Equals Selector Selects an element if the given attribute value exactly matches the value stated
a[href*="login"]  Attribute Contains Selector Selects an element if the given attribute value contains at least once instance of the value stated

a[href^="https://"] Attribute Begins With Selector  Selects an element if the given attribute value begins with the value stated

a[href$=".pdf"] Attribute Ends With Selector  Selects an element if the given attribute value ends with the value stated

a[rel~="tag"] Attribute Spaced Selector Selects an element if the given attribute value is whitespace-separated with one word being exactly as stated

a[lang|="en"] Attribute Hyphenated Selector Selects an element if the given attribute value is hyphen-separated and begins with the word stated

*Pseudo-classes

Pseudo-classes are similar to regular classes in HTML however they are not directly stated within the markup, instead they are a dynamically populated as a result of users actions or the document structure. The most common pseudo-class, and one you’ve likely seen before, is :hover. Notice how this pseudo-class begins with the colon character, :, as will all other pseudo-classes.

a:link {...}
a:visited {...}

*User Action Pseudo-classes

a:hover {...}
a:active {...}
a:focus {...}


*User Interface State Pseudo-classes

input:enabled {...}
input:disabled {...}

input:checked {...}
input:indeterminate {...}


*Structural & Position Pseudo-classes

A handful of pseudo-classes are structural and position based, in which they are determined based off where elements reside in the document tree. These structural and position based pseudo-classes come in a few different shapes and sizes, each of which provides their own unique function. Some pseudo-classes have been around longer than others, however CSS3 brought way of an entire new set of pseudo-classes to supplement the existing ones.

:first-child, :last-child, & :only-child

The first structural and position based pseudo-classes one is likely to come across are the :first-child, :last-child, and :only-child pseudo-classes. The :first-child pseudo-class will select an element if it’s the first child within its parent, while the :last-child pseudo-class will select an element if it’s the last element within its parent. These pseudo-classes are prefect for selecting the first or last items in a list and so forth. Additionally, the :only-child will select an element if it is the only element within a parent. Alternately, the :only-child pseudo-class could be written as :first-child:last-child, however :only-child holds a lower specificity.

Here the selector li:first-child identifies the first list item within a list, while the selector li:last-child identifies the last list item within a list, thus lines 2 and 10 are selected. The selector div:only-child is looking for a division which is the single child of a parent element, without any other other siblings. In this case line 4 is selected as it is the only division within the specific list item.

CSS

li:first-child {...}
li:last-child {...}
div:only-child {...}


ul>
  li>This list item will be selected</li>
  li>
    div>This div will be selected</div>
  /li>
  li>
    div>...</div>
    div>...</div>
  /li>
  li>This list item will be selected</li>
/ul>

:first-of-type, :last-of-type, & :only-of-type

p:first-of-type {...}
p:last-of-type {...}
img:only-of-type {...}


article>
  h1>...</h1>
  p>This paragraph will be selected</p>
  p>...</p>
  img src="#"><!-- This image will be selected -->
  p>This paragraph will be selected</p>
  h6>...</h6>
/article>


*:nth-child(n) & :nth-last-child(n)

li:nth-child(3n) {...}

ul>
  li>...</li>
  li>...</li>
  li>This list item will be selected</li>
  li>...</li>
  li>...</li>
  li>This list item will be selected</li>
/ul>

*:nth-of-type(n) & :nth-last-of-type(n)

p:nth-of-type(3n) {...}

*Target Pseudo-class

The :target pseudo-class is used to style elements when an element’s ID attribute value matches that of the URI fragment identifier. The fragment identifier within a URI can be recognized by the hash character, #, and what directly follows it. The URL http://example.com/index.html#hello includes the fragment identifier of hello. When this identifier matches the ID attribute value of an element on the page, <section id="hello"> for example, that element may be identified and stylized using the :target pseudo-class. Fragment identifiers are most commonly seen when using on page links, or linking to another part of the same page.

section:target {...}


section id="hello">...</section>

web  complet selectors: http://learn.shayhowe.com/advanced-html-css/complex-selectors/


Absolute length units

px
Relative to the viewing device.
For screen display, typically one device pixel (dot) of the display.
For printers and very high resolution screens one CSS pixel implies multiple device pixels, so that the number of pixel per inch stays around 96.

mm
One millimeter

q
A quarter of a millimeter (1/40th of a centimeter).

cm
One centimeter (10 millimeters).

in
One inch (2.54 centimeters).

pt
One point (1/72nd of an inch).

pc
One pica (12 points).


Relative length units

em
Represents the calculated font-size of the element. If used on the font-size property itself, it represents the inherited font-size of the element.

ex
Represents the x-height of the element's font. On fonts with the 'x' letter, this is generally the height of lowercase letters in the font; 1ex ≈ 0.5em in many fonts.

cap
Represents the "cap height" (nominal height of capital letters) of the element’s font

ch
Represents the width, or more precisely the advance measure, of the glyph '0' (zero, the Unicode character U+0030) in the element's font.


*CSS3 Positioning

The Box Model [1]
width, height, padding, margin, border
box-sizing: border-box;

CSS3 box-sizing Property
Definition and Usage
The box-sizing property is used to tell the browser what the sizing properties (width and height) should include.

Relative Positioning

The relative value for the position property allows elements to appear within the normal flow a page, leaving space for an element as intended while not allowing other elements to flow around it; however, it also allows an element’s display position to be modified with the box offset properties. For example, consider the following HTML and CSS:

static, 
relative.
fixed,
absolute, 
z index,

Centering in CSS: A Complete Guide

https://css-tricks.com/centering-css-complete-guide/

Flexbox

https://css-tricks.com/snippets/css/a-guide-to-flexbox/

flex-direction: row | row-reverse | column | column-reverse;

 flex-wrap: nowrap | wrap | wrap-reverse;

 *MediaQuery

 Media Queries is a module of CSS that defines expressions allowing to tailor presentations to a specific range of output devices without changing the content itself.

 ReferenceEDIT
At-rules

@import
@media


*Class 8

CSS3 Effects & Animation

@font-face {
  font-family: 'MyWebFont';
  src: url('webfont.eot'); /* IE9 Compat Modes */
  src: url('webfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('webfont.woff2') format('woff2'), /* Super Modern Browsers */
       url('webfont.woff') format('woff'), /* Pretty Modern Browsers */
       url('webfont.ttf')  format('truetype'), /* Safari, Android, iOS */
       url('webfont.svg#svgFontName') format('svg'); /* Legacy iOS */
}
This is the method with the deepest support possible right now. The @font-face rule should be added to the stylesheet before any styles.

Then use it to style elements like this:

body {
  font-family: 'MyWebFont', Fallback, sans-serif;
}


Alternative Techniques

While @font-face is excellent for fonts that are hosted on our own servers, there may be situations where a hosted font solution is better. Google Fonts offers this as a way to use their fonts. The following is an example of using @import to load the Open Sans font from Google Fonts:

@import url(//fonts.googleapis.com/css?family=Open+Sans);

Then we can use it to style elements:

body {
  font-family: 'Open Sans', sans-serif;
}

<link>ing a stylesheet
Similarly, you could link to the same asset as you would any other CSS filter, in the <head> of the HTML document rather than in the CSS. Using the same example from Google Fonts, this is what we would use:

<link href='//fonts.googleapis.com/css?family=Open+Sans' rel='stylesheet' type='text/css'>
Then, we can style our elements like the other methods:

body {
  font-family: 'Open Sans', sans-serif;
}


*text-overflow

The text-overflow property in CSS deals with situations where text is clipped when it overflows the element's box. It can be clipped (i.e. cut off, hidden), display an ellipsis ('…', Unicode Range Value U+2026) or display an author-defined string (no current browser support for author-defined strings).

.ellipsis {
  text-overflow: ellipsis;

  /* Required for text-overflow to do anything */
  white-space: nowrap;
  overflow: hidden;
}


.clip { text-overflow: clip; }
This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.

.ellipsis { text-overflow: ellipsis; }
This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.

.word { text-overflow: ellipsis-word; }
This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.

.text { text-overflow: "---"; }
This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.

.double { text-overflow: ellipsis ellipsis; text-align: center; }
This is an example text showing no

.. ejemplo: https://css-tricks.com/almanac/properties/t/text-overflow/

word-break

The word-break CSS property specifies whether or not the browser should insert line breaks wherever the text would otherwise overflow its content box. In contrast to overflow-wrap, word-break will create a break at the exact place where text would otherwise overflow its container (even if putting an entire word on its own line would negate the need for a break).

1. word-break: normal

This is a long and Supercalifragilisticexpialidocious sentence. 次の単語グレートブリテンおよび北アイルランド連合王国で本当に大きな言葉

2. word-break: break-all

This is a long and Supercalifragilisticexpialidocious sentence. 次の単語グレートブリテンおよび北アイルランド連合王国で本当に大きな言葉

3. word-break: keep-all

This is a long and Supercalifragilisticexpialidocious sentence. 次の単語グレートブリテンおよび北アイルランド連合王国で本当に大きな言葉

ejemplo: https://developer.mozilla.org/es/docs/Web/CSS/word-break

box-shadow

ejemplo: https://css-tricks.com/almanac/properties/b/box-shadow/

.shadow {
  -webkit-box-shadow: 3px 3px 5px 6px #ccc;  /* Safari 3-4, iOS 4.0.2 - 4.2, Android 2.3+ */
  -moz-box-shadow:    3px 3px 5px 6px #ccc;  /* Firefox 3.5 - 3.6 */
  box-shadow:         3px 3px 5px 6px #ccc;  /* Opera 10.5, IE 9, Firefox 4+, Chrome 6+, iOS 5 */
}

box-shadow: [horizontal offset] [vertical offset] [blur radius] [optional spread radius] [color];

The horizontal offset (required) of the shadow, positive means the shadow will be on the right of the box, a negative offset will put the shadow on the left of the box.

The vertical offset (required) of the shadow, a negative one means the box-shadow will be above the box, a positive one means the shadow will be below the box.

The blur radius (required), if set to 0 the shadow will be sharp, the higher the number, the more blurred it will be, and the further out the shadow will extend. For instance a shadow with 5px of horizontal offset that also has a 5px blur radius will be 10px of total shadow.

The spread radius (optional), positive values increase the size of the shadow, negative values decrease the size. Default is 0 (the shadow is same size as blur).

Color (required) - takes any color value, like hex, named, rgba or hsla. If the color value is omitted, box shadows are drawn in the foreground color (text color). But be aware, older WebKit browsers (pre Chrome 20 and Safari 6) ignore the rule when color is omitted.


border-radius

#example-one {
  border-radius: 10px;
  background: #BADA55;
}
#example-two {
  border-radius: 10px;
  border: 3px solid #BADA55;
}

ejemplo: https://css-tricks.com/almanac/properties/b/border-radius/

*Opacity 

Definition and Usage
The opacity property sets the opacity level for an element.

The opacity-level describes the transparency-level, where 1 is not transparent at all, 0.5 is 50% see-through, and 0 is completely transparent.

ejemplos: https://www.w3schools.com/cssref/css3_pr_opacity.asp

*filter


Using just CSS you are able to create all these effects on images.

Greyscale
Blur
Saturate
Sepia
Hue Rotate
Invert
Brightness
Contrast
Opacity

How To Use Filters
To use a filter in CSS it's as easy as using any other CSS property.
img
{
     filter: type(value);
}
Like most of new features in CSS3 you need to use browser prefixes.
img
{
     filter: type(value);
     -webkit-filter: type(value);
     -moz-filter: type(value);
     -ms-filter: type(value);
     -o-filter: type(value);
}

and more.

ejemplos: https://paulund.co.uk/css-filter


*Transformations 

Transform Syntax
The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}

.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}


etc.. 
ejemplos: http://learn.shayhowe.com/advanced-html-css/css-transforms/#transform-syntax


*Transitions & Animations

As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes

.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

Animations Keyframes

To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

ejemplo: http://learn.shayhowe.com/advanced-html-css/transitions-animations/


*Class 9

WHY IS BOOTSTRAP IMPORTANT?

As mentioned above, Bootstrap is so amazing because it has been created as mobile-first. As Caitlin points to,

“With the number of people browsing the internet on their phone or tablet increasing steadily, it’s important to optimize websites for both the desktop and mobile browsing experience.”

Bootstrap embodies the present and future of the web: the ability to work seamlessly on both large desktop monitors and small mobile screens.

*Understanding the Bootstrap 3 Grid System

Bootstrap 2

The grid you create works on desktops and then stacks on top of each other when browser size is below 767px. This is limited since you can only define 1 grid on desktop sized browsers. You are left with a stacked grid on mobile devices.

Bootstrap 3

The new Bootstrap grid system applies to mobile first. When you declare a specific grid size, that is the grid for that size and above. This can be a little hard to grasp at first so here's an example.

For example, let's say you want a site that has:

1 column on extra small devices
2 columns on small AND medium devices
4 columns on large devices

.col-xs-$ Extra Small Phones Less than 768px
.col-sm-$ Small Devices Tablets 768px and Up
.col-md-$ Medium Devices  Desktops 992px and Up
.col-lg-$ Large Devices Large Desktops 1200px and Up

Example: Fluid container
Turn any fixed-width grid layout into a full-width layout by changing your outermost .container to .container-fluid


Offsetting columns
Move columns to the right using .col-md-offset-* classes. These classes increase the left margin of a column by * columns. For example, .col-md-offset-4 moves .col-md-4 over four columns.

ejemplos: http://getbootstrap.com/css/#grid-options



