# Entry 5: Compnents Interacting

## Notes On What I learned
### Components Render Other Components
The point of this unit was to demonstrate how to connect files together. With ```require ('./NavBar.js');```,
the information all pages will have NavBar shown across. This will be easy access to not repeat the same 
code for every single page.

1. Making a ```<ProfilePage />``` render a ```<NavBar />```:
```javascript
var NavBar = require ('./NavBar.js'); //this imports NavBar.js

var ProfilePage = React.createClass({
  render: function () {
    return (
      <div>
		<NavBar /> //
        <h1>All About Me!</h1>
        <p>I like movies and blah blah blah blah blah</p>
        <img src="https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-monkeyselfie.jpg" />
      </div>
    );
  }
});
```
2. Using ```module.exports = NavBar;``` at the bottom of the file with the NavBar.js components, will 
get back exactly what it wants: the NavBar component class.
```javascript
var React = require('react');

var NavBar = React.createClass({
  render: function () {
    var pages = ['home', 'blog', 'pics', 'bio', 'art', 'shop', 'about', 'contact'];
    //these are the links on the navagation bar
    var navLinks = pages.map(function(page){
      return (
        <a href={'/' + page}> //links
          {page}
        </a>
      );
    });
    return <nav>{navLinks}</nav>;
  }
});

module.exports = NavBar; //moves all functions to one file
```
3. Render ```ReactDOM.render(<ProfilePage />, document.getElementById('app'));``` at the bottom of the 
Profile page to show up on screen.

### Components Interacting
1. ```props``` holds information about a component(s). When injecting a variable in tags such as h1,
be sure to put brackets {}. Ex. ```<h1>{stringProps}</h1>``` Now all the props that stringProps holds
will be displayed. (kinda like an array)
2. Passing information to a React Component can be done by using attributes! You can even write it inside
the render: ```ReactDOM.render(<PropsDisplayer myProp="Hello"/>, document.getElementById('app'));```
3. ```{this.props.name-of-information}``` which is placed inside a tag will holds information about 
the component.
4. Passing a prop from one component to another. This can be useful when you want to transfer information:
    - remove ```var ReactDOM = require('react-dom');``` so not all information is entirely fixed.
    - instead of render, do ```module.exports = Greeting; ```
    - Add ```var ReactDOM = require('react');``` and ```var Greeting = require('./Greeting');``` in Apps.js
    - Put ```<Greeting name="daphne" />``` inside of Apps.js's return function
As long as the information is opposing each file and the var-require is linked, then you can pass a prop!
5. Using props to make a decision: This can be done through making true/false methods. For ex.:
```
 <Greeting name="Alison" signedIn={true} />
```
This code is inside Apps.js and when signedIn = false, then the screen will pop up a different response.
6. To pass an event handler function as a prop:
    - make ```var Talker = React.createClass({     });``` cover your entire code
    - instead of ```function talk ()```, do ``` talk: function ()```. This referrs to the multiple variables the component consists.
7. To pass talk from ```<Talker />``` to ```<Button />```, you only need to change the render's return fuction from
'foo' (the original attribute) to 'talk' and the information to be 'this.talk'.
8. A button with an attribute (```<button onClick = {this.props.talk}>```) can transfer the informaiton
from the talk file to the screen with a click of a button. I thought this is very neat and organizing 
and it is different from regular javascript where we have to put in all the information into the button.
9. 

## Takeaways
* Some of the Codecademy work was difficult to work with, but luckily the program allows me to see the answer when
I get multiple lines of error. For instance, in step 6 of my Components Interacting unit, I found out that copying 
the old code and right code and viewing them side by side to be helpful.
```
function talk () {
  for (var speech = '', i = 0; i < 10000; i++) {
    speech += 'blah ';
  }
  alert(speech);
}

var Talker = React.createClass({
  render: function () {
    return <Button />;
  }
});
---------------------------
var Talker = React.createClass({
  talk: function () {
    for (var speech = '', i = 0; i < 10000; i++) {
      speech += 'blah ';
    }
    alert(speech);
  },
  
  render: function () {
    return <Button />;
  }
});
```
* Since I've finished Codecademy right now, my next steps is to start my layout for my project. I will
start out simple with JSX that I learned during the beginning of the Codecademy.
