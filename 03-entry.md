# Entry 3: React Components
I had justed finished learning about the JSX part of ReactJS of the Codeacademy lesson and now I am moving
on to the second part which is learning the React components!

## Notes On What I Learned 
### Your First React Components
1. Every component must come from a component class. A component class is like a factory that creates 
components. If you have a component class, then you can use that class to produce as many components 
as you want: ```React.createClass();```
2. To store the result of React.createClass(); in a variable: ```MyComponentClass = React.createClass();```
3. How to render / return a JSX function
```
var componentBlueprint = {
  render: function () {
    return <h1>Hello world</h1>;
  }
};
```