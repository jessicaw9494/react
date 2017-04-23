# Entry 4: React Components Continued

## Notes On What I Learned
### Components and Advanced JSX
1. This makes HTML appear in ReactJS code. Making a React component that renders HTML with Quotemaker:
```javascript
var QuoteMaker = React.createClass({
  render: function () {
    return (
      <blockquote>
  <p>
    What is important now is to recover our senses.
  </p>
  <cite>
    <a target="_blank" 
      href="http://bit.ly/1LvSLUA">
      Susan Sontag
    </a>
  </cite>
</blockquote>
    );
  }
});
```
2. I found all these steps to be quite arudous just to make an image appear. However, I can see how this
can be useful to access multiple images in one div with a short name rather than uploading the image 
to c9 first. To make an image appear:
```javascript
var owl = {
  title: "Excellent Owl",
  src: "https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-owl.jpg"
};

// Component class starts here:
var Owl = React.createClass({
  render: function () {
  var friend= friends[0] //you can also make a new variable inside of render
    return (
      <div>
       	<h1>
          {owl.title} //use curly braces to access owl.title
        </h1>
        <img 
          src ={owl.src}
          alt ={owl.title} />
      </div>
    );
  }
});

ReactDOM.render(<Owl />, document.getElementById('app'));
```
3. This code is actually connected to another tab that to make the code run shorter. Creating 
a shortcut of an if/else statement:
```javascript
//this code is the layout
var TodaysPlan = React.createClass({
  render: function () {
    var task;
    if (!apocalypse) {
      task = "learn React.js"
    } else {
      task = "run around"
    }

    return <h1>Today I am going to {task}!</h1>;
  }
});
```
```javascript
var TonightsPlan = React.createClass({
  render: function () {
    var place = fiftyFifty ? 'out' : 'to bed'; //if fiftyFifty is true, then TonightsPlan render h1
    return <h1>Tonight I'm going {place} WOOO</h1>;
  }
});

ReactDOM.render(
  <TonightsPlan />,
  document.getElementById('app')
);
```
4. ```this``` refers to the instructions object being passed to React.createClass.
```javascript 
var MyName = React.createClass({
name: 'jess', //sets the string 
  render: function () {
    return <h1>My name is {this.name}.</h1>; //replaces the name with what you had set to
  }
});
```
5. Making a popup alert with a click of a button:
```javascript
var Button = React.createClass({
  scream: function () {
    alert('AAAAAAAAHHH!!!!!');
  },

  render: function () {
    return <button onClick ={this.scream}>AAAAAH!</button>; 
    //you can make diff attributes inside of button ex. onClick, onHover...and then run the code
  }
});
```
## Takeaways 
* Always render the code after you've finished. Throughout the lesson, there were times when I forgot 
to render which created an error.
