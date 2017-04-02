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

## Takeaways
* Read everything that is provided on the Codeacademy left hand corner.
* Quizzes are very good a summarizing everything in the lesson you just learned.
