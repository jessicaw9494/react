# Entry 8: Working on code

## MVP Plan
Right now, before I could do any touches on the background, I think that I need to make the game interactive
by making my tennis ball bounce. I will have the tennis ball touch the player, and then move back into position.
I already have my countdown working, but I need to make only the number change instead of showing paragraphs. 

Ok, my first step right now is to make my countdown consistent. Right now my code is making consecutive paragraphs 
appearing, but I only want there to be one sentence with the number changing. I started looking at this code:
```javascript
onPress = () => {
    let hit = [ ...this.state.hit ];
    hit.push(`You've scored ${this.state.hit.length} times!`)
    this.setState({ hit });
  }
```
I realized that ```.push``` is making this code repeat, because when I removed it and changed it to .state,
the code does not appear on my screen anymore, but on the console.log.

### Problem(s)
- [ ] I need to figure out how to make my scorekeeper consistent.

Before I could get the final product, I am deciding to make the tennis ball image into a gif.
For instance right now, I have a player and a tennis ball gif. Once I press the button for Let's Play Tennis,
I will change the image frames to once image: a tennis racket with a ball. 

## Takeaways
I am planning on using an if/else statement where the image will change once I click onPress as my final project.
I found that my original plan of having a ball bouncing in different directions to be too much. I will have
the simple steps of 

### Problem(s)
- [ ] I need to have my images change once I press the button.