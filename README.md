

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




