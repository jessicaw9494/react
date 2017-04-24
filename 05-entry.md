# Entry 5: Compnents Interacting

## Notes On What I learned
### Components Render Other Components
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

module.exports = NavBar;
```
3. Render ```ReactDOM.render(<ProfilePage />, document.getElementById('app'));``` at the bottom of the 
Profile page to show up on screen.
![entry5firstex](/react/entry5firstex.png)

## Takeaways
* Since I've finished Codecademy right now, my next steps is to start my layout for my project.
* 