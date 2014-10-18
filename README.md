[![NPM](https://nodei.co/npm/vz.rand.png?downloads=true)](https://nodei.co/npm/vz.rand/)

This package uses or may use at some point in the future ECMAScript 6 features. Use it on a compatible environment or transpile it with Traceur, Closure Compiler, es6-transpiler or equivalent. Please note that some of these have flaws and bugs, test your code carefully until you find a suitable tool for your task.

When cloning this repository, put the folder inside another named "node_modules" in order to avoid potential errors related to npm's dependency handling, and then run `npm install` on it.

No piece of software is ever completed, feel free to contribute and be humble.

# vz rand

## Sample usage:

```javascript

var rand = require('vz.rand');

rand(5);                  // Integer in the interval [0,5)
rand(0,6);                // Integer in the interval [0,6)
rand(0,6,true);           // Float in the interval [0,6)
rand.string(20);          // String of 20 characters, combination of 0-9a-z
rand.string(20,true);     // Same as above, but including date information
rand.string(20,62);       // String of 20 characters, combination of 0-9a-zA-Z
rand.string(20,62,true);  // Same as above, but including date information

```

## Reference

### rand(start[,end][,dontTruncate])

Returns a random number starting at *start*, up to, but not including, *end*. Unless *dontTruncate* is present and true, integers are returned. If *end* is not specified, and *start* is positive, *start* is treated as end and 0 is treated as start. If it's negative, 0 is treated as end.

### rand.string(n[,base][,useDate])

Returns a random string of length *n*, using up to *base* different characters - 36 by default - and including a timestamp if *useDate* evals to true.
