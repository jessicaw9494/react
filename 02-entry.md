# Entry 2: Learning on Codeacademy
Before I can create an app, I need to learn React JS! I found out that Codecademy teaches React JS.

## Notes On What I Learned
### JSX Element
JSX is a preprocessor step that adds XML(stores data) syntax to JavaScript and it makes React more elegant. So far
in the basics that I have learned, this is how you make text appear from JSX to the screen:
1. To create a JSX element, it's basically like html: ```<article></article>```
2. To save the element into a variable ```var myArticle = <article></article>```
3. To set an id, you can do it like html ```var myArticle = <article id="news"></article>```
4. A JSX expression with multiple outer elements must be wrapped with a ```<div>```.
```var paragraphs = (<div><p>I am a paragraph.</p></div>);```
5. To render a JSX expression (make it appear onscreen) ```ReactDOM.render(variableName, document.getElementById('app'));```
6. ReactDOM.render only updates DOM elements that have changed.
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

## Takeaways
* Read everything that is provided on the Codeacademy left hand corner.
* Quizzes are very good a summarizing everything in the lesson you just learned.
