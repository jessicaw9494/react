# Entry 3: React Components
I had justed finished learning about the JSX part of ReactJS of the Codeacademy lesson and now I am moving
on to the second part which is learning the React components!

## Notes On What I Learned 
### Advanced JSX
Advanced JSX is a bit simplier compared to JSX.
1. self-closing tags (you do not need the slash to close) ```<div> blahblahblah <div>```
2. Using curly brackets will make the element in an ```<h1></h1>``` will write the code:
```
ReactDOM.render(
  <h1>2 + 3</h1>,
  document.getElementById('app')
);
```
  this will give me the value 5.
3. You can make only part of the element a string and the other part to put out by:
```var math = <h1>2 + 3 = {2 + 3}</h1>```
4. You can also make a variable equalled to a string appear by using a ```<h1>``` in your Render's first
argument.
5. Event listener names in JSX are written in camelCase, such as onClick or onMouseOver.
6. Using an if/else statement has it's own open and close brackets
```
if (coinToss() == 'heads') {
  var img = <img src={pics.kitty} />;
} else {
  var img = <img src={pics.doggy} />;
}
```
7. Writing conditions: ```var img = <img src={pics[coinToss() == 'heads' ? 'kitty' : 'doggy']} />;```
8. ```{ !judgmental && <li>Nacho Cheez Straight Out The Jar</li> }```
9. Returning a parameter ```return <li>{parameter}</li>```
10. ```key``` is similar to ```id```.
11. Rewrite React code without using JSX at all:
```var h1 = <h1>Hello world</h1>;```
```
var h1 = React.createElement(
  "h1",
  null,
  "Hello, world"
);
```
  1st argument-```<h1>``` into "h1"   
  2nd arument-null  
  3rd arugment-the string
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
4. Creating an instance: ```<MyComponentClass />``` (You put this below your variables.)
```
ReactDOM.render(
  <MyComponentClass />,
  document.getElementById('app')
);
```

## Takeaways
* To keep up with the time frame, I decide to catch up on my Codeacademy lessons and finish a unit every week.
* I thought this unit is getting more useful as games consists of many conditionals. For the tennis game I am
planning, 