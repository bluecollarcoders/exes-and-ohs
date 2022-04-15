# exes-and-ohs

## Problem
Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.

Examples input/output:

XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false
FUNDAMENTALS

## Solution 1
```javascript
const XO = (str) => {
// assign variable for x value
let countX = '';
// assign variable for o value
  let countO = '';
// run for loop
  for (let i=0; i<str.length; i++) {
//     conditional statement 
    if (str[i].toLowerCase() === 'x') {
      countX += str[i];
      } else if (str[i].toLowerCase() === 'o') {
      countO += str[i];
      }
    }
    return countX.length === countO.length ;
};
```
## Solution 2
```javascript
const XO = (str) => {
var count = 0;
for (let char of str) {
  if(char.toLowerCase() == 'x') count++;
  if(char.toLowerCase() == 'o') count--;
}
  return count == 0;
};
```

