## Forms in react. 
-  In React, a state is  kept in the state property of components, and only updated with setState().
- we can make the form and state property work together if we make the state the "single source of truth" 
- the component that renders the form will controle what happens depending in the users input.
-  the controlled component is the input value of forms that is controlled bt react.
- the input’s value is always driven by the React state. (from reactjs.org)
- we should update the state in a controlled component because you only need to update it in one place.
--------------------- 
- ternart operation is a way to shorten code: 
instead of writing this:

```javascript

if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}

```
- you can write this :

```javascript

person.driver = person.age >=16 ? 'Yes' : 'No';
```
- the syntax: condition ? value if true : value if false
instead of doing this :
```javascript 
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
  ```
  - you can make :

  ```javascript 
  var.sth? var2 x===y : 'true' : 'false';
