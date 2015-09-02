# ECMAScript 6

## What is ECMAScript?

ECMAScript is the specification and language standard for JavaScript.  It is formally known as EMCA-262.  It is defined by ECMA International and more specifically the TC39 (Technical Committee) within ECMA.  The committee consists of a representative from each browser vendor and other parties that have an interest in the specification.

The people on the committee are in charge of making new features, additions, and also standardizing the next version of the language.  

### Brief History of ECMAScript

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

[Mortgage Calculator Application](http://coenraets.org/apps/react-mortgage-calc/) by Christophe Coenraets
Uses ECMAScript 6, React, and Babel

(He actually teaches this as an [ES6 tutorial](http://coenraets.org/blog/2015/07/building-react-applications-with-babel-ecmascript-6-and-modules/) online)

## Code Examples

### Constants

##### ES5
```JavaScript
// only in ES5 through the help of object properties
// and only in global context and not in a block scope
Object.defineProperty(typeof global === "object" ? global : window, "PI", {
    value:        3.141593,
    enumerable:   true,
    writable:     false,
    configurable: false
})
console.log(PI > 3.0); //true
```

#### ES6
```JavaScript
const PI = 3.141593;
console.log(PI > 3.0); //true

const COLOR = {
    name: “Red”,
    hexValue: “#FF0000”
};
```