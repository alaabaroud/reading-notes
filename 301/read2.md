## what sre the lifecycle events in react ?
- lifecycle events are the methods that you use, and it can be used (called) during the lifecycle of a component.
- there are three phases for this: 
    - mounting: when we create a component and inserted it it will be shown during mounting.
    - Updating: when any updates happen to the components.
    - unmounting: when the component is removed.

- the componentDidMount comes after rendering, this method is used to load anything using a network or initializting DOM. 
 // medium.com//
- the right order for it :
- constructor
-react Updates
- render()
- componentDidUpdate()
- componentWillUnmount()
---------------------------

- props pass like functions.
- the difference betweet props and state is that : 
    - props passes to the component
    - states is handled inside the component itself.
- we rerender the application when we have changes in the props.
- we can store data in states such as strings numbers and objects.

