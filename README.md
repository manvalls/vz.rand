
**DEPRECATED in favour of [u-rand](https://www.npmjs.org/package/u-rand "u-rand")**

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
