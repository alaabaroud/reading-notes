## .map():


- using the map method is a way to shorten the code.
- it returns a new array with the same length of the array that it is working with.
- each list item has to have a key ti identify it. and to make it unique.
- keys give the elements an identity 


```javascript
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);

```
**this code is from reactjs.org**

## The spread operator
- it is a way to add items to an array real quick and spreading it out to the functions.
- we can make it by adding three dots ... 
- “When ...arr is used in the function call, it ‘expands’ an iterable object arr into the list of arguments.” — **from JavaScript.info**
- it spreads the array to a separate arguments.
- it can do many thinds as well : 
    - Copying an array
    - Adding an item to a list
    - Using Math functions
    - Combining objects
and many other things.. 

-----------------------
