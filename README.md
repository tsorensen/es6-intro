ECMAScript 6
===

### What is ECMAScript?

ECMAScript is the specification and language standard for JavaScript.  It is formally known as <a href="http://www.ecma-international.org/publications/standards/Ecma-262.htm" target="_blank">EMCA-262</a>.  It is defined by ECMA International and more specifically the TC39 (Technical Committee) within ECMA.  The committee consists of a representative from each browser vendor and other parties that have an interest in the specification.

The people on the committee are in charge of making new features, additions, and also standardizing the next version of the language specification.  

| Editions      | Release Year  |
| ------------- |:-------------:|
| ECMAScript 1  | 1991          |
| ECMAScript 2  | 1998          |
| ECMAScript 3  | 1999          |
| ECMAScript 4  | (abandoned)   |
| ECMAScript 5  | 2009          |
| ECMAScript 6  | (drafting)    |

### Goals with ECMAScript 6

* Better support for complex applications, libraries, and code generators
* Avoid fragmentation around core language features (see more about ECMAScript 6 modules, promises, classes, etc.)
* Backward compatibility

## Example Application

<a href="http://coenraets.org/apps/react-mortgage-calc/" target="_blank">Mortgage Calculator Application</a> by Christophe Coenraets <br>
He uses ECMAScript 6, <a href="http://facebook.github.io/react/" target="_blank">React</a>, and <a href="https://babeljs.io/" target="_blank">Babel</a>

(He actually teaches this as an <a href="http://coenraets.org/blog/2015/07/building-react-applications-with-babel-ecmascript-6-and-modules/" target="_blank">ES6 tutorial</a> online)

## Code Examples

### Constants

Instead of global constants that could only be created with the help of object properties, you can now easily declare constants with `const` that are block-scoped.

###### ES5
```JavaScript
Object.defineProperty(typeof global === "object" ? global : window, "PI", {
    value:        3.141593,
    enumerable:   true,
    writable:     false,
    configurable: false
})
console.log(PI > 3.0); //true
```

###### ES6
```JavaScript
const PI = 3.141593;
console.log(PI > 3.0); //true

const COLOR = {
    name: "Red",
    hexValue: "#FF0000"
};
```

### Let

Instead of changing `var` (for backward compatibility), ES6 introduces `let`, which allows you to declare variables that are block-scoped.

###### ES5
```JavaScript
for(var i = 0; i < 10; i++) {
   console.log(i);
}
console.log(i); //10
```

###### ES6
```JavaScript
for(let i = 0; i < 10; i++) {
   console.log(i);
}
console.log(i) //error not defined
```

### Creating objects from variables 

The new syntax for creating objects from variables is simpler and quicker.

###### ES5
```JavaScript
var firstName = "John";
var lastName = "Smith";
var email = "john@site.com";

var info = {
    firstName: firstName,
    lastName: lastName,
    email: email 
}
```

######ES6
```JavaScript
var firstName = "John";
var lastName = "Smith";
var email = "john@site.com";

var fullName = {firstName, lastName, email};
```

### Deconstructing

Deconstructing also has a new syntax that is quicker.

###### ES5
```JavaScript
var colors = ["red", "green", "blue"];

var primary = colors[0];
var secondary = colors[1];
var tertiary = colors[2];

console.log(primary); //red
console.log(secondary); //green
console.log(tertiary);  //blue
```

###### ES6
```JavaScript
var colors = ["red", "green", "blue"];

var [primary, secondary, tertiary] = colors;

console.log(primary); //red
console.log(secondary); //green
console.log(tertiary);  //blue
```

### Arrow Functions

Arrows are the new shorthand for writing functions.  Also, they share the same <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#Lexical_this" target="_blank">lexical this</a>, so `var self=this;` is no longer necessary.

###### ES5
```JavaScript
var reflect = function(value) {
	return value;
}

var double = function(num1, num2) {
	return num1 * num2;
}

console.log(double(2, 2)); //4
```

###### ES6
```JavaScript
var reflect = value => value;

var double = (num1, num2) => num1 * num2;

console.log(double(2, 2)); //4
```

### Default Parameters

Like a lot of other programming languages, defualt parameters are now supported.

###### ES5
```JavaScript
function greeting(message, name) {
  name = name || 'Anonymous';
  return message + " " + name;
}
```
###### ES6
```JavaScript
function greeting(message, name = 'Anonymous') {
  return message + " " + name;
}
```

### Template Strings

In ES6, some syntactic sugar was added for constructing strings.  Similar to string interpolation in Ruby, Python, etc.

###### ES5
```JavaScript
var name = "John";
var time = "afternoon";

var greeting = 'Hello ' + name + ', how are you this ' + time + '?';
console.log(greeting); //Hello John, how are you this afternoon?
```
###### ES6 
```JavaScript
var name = "John";
var time = "afternoon";
 
var greeting = 'Hello ${name}, how are you this ${time}?';
console.log(greeting); //Hello John, how are you this afternoon?
```

## Resources 

* Popular Transpilers (<a href="https://babeljs.io/" target="_blank">BabelJS</a>, <a href="https://github.com/google/traceur-compiler" target="_blank">Traceur</a>)
* <a href="http://ccoenraets.github.io/es6-tutorial/" target="_blank">Christophe Coenraets ES6 tutorial</a>
* <a href="https://github.com/lukehoban/es6features" target="_blank">Luke Hoban ES6 Features</a>
* <a href="https://www.sencha.com/blog/toward-modern-web-apps-with-ecmascript-6-2/" target="_blank">Sencha - Modern web apps with ES6</a>
* <a href="http://es6-features.org/#DefaultParameterValues" target="_blank">es6-features.org</a>
* <a href="https://en.wikipedia.org/wiki/ECMAScript#4th_Edition_.28abandoned.29" target="_blank">ECMAScript on Wikipedia</a> 
* <a href="http://www.ecma-international.org/" target="_blank">ECMA International</a>
* <a href="http://www.ecma-international.org/ecma-262/6.0/" target="_blank">ECMA International ES6 Draft</a> 
* <a href="http://codeutopia.net/blog/2015/01/06/es6-what-are-the-benefits-of-the-new-features-in-practice/" target="_blank">CodeUtopia - article on ES6 features</a> 
* <a href="http://kangax.github.io/compat-table/es6/" target="_blank">ES6 Compatibility Table</a> 

