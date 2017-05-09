# Entry 6: Brainstorming for App

## How to begin:
I am planning on using repl.it with React Native. The difference between React Native and ReactJS is that
React Native is the mobile framework and ReactJS is the language. 
When starting with React, I needed to scan a QR code to preview my code. 

I read [Repl Blog](https://repl.it/site/blog/react_native) and 
[Making ReactJS without QR code](https://www.npmjs.com/package/qrcode.react) as reference to getting started.
Since it's inconvienent to scan a QR code everytime I run, I tried to look for a method in which I could 
preview online. However, since I want my game to be an atual app, I thought it would be better to use the QR code
which would be easy reference and automatic app. Furthermore, the transfer from code that is online to phone may
cause bugs.

<iframe src='https://gfycat.com/ifr/PepperyIllfatedGerbil' frameborder='0' scrolling='no' width='640' height='360' allowfullscreen></iframe>

Using the Chewbacca game as an example I was able to create an outline for my game. So far I am able to make the 
tennis ball to appear with how many times scored with an onPress command.
```javascript
render() { //run
    return (
      <View style={styles.container}>
        <Image 
          source={{uri: "https://lh5.googleusercontent.com/-VyZDpd_dTIo/VDtes4mCmOI/AAAAAAAAADQ/psSjLdQD_Ww/w1826-h1826/MTO_Tennis_Ball.png"}}
          style={{width: 150, height: 150}} //image
        />
        <Button title="Let's Play Tennis" onPress={this.onPress} /> 
        {this.state.hit.map(r => <Text style={styles.paragraph}>{r}</Text>)}
      </View> 
    ); //what's written on the button
  }
}
```
<img src="http://i.imgur.com/nwETCvV.png" width="250" height="400" />

Probably the most challenging part of the app is to make it interactive. Here's my plan:
* Make the tennis ball appear randomly. I plan on referring to this game, [Reactoroids](https://react.rocks/example/Reacteroids),
that makes different shapes of rocks appear at a random place.
* Make a default tennis ball on the top side of the screen. When the bouncing tennis ball touches it, it will then
move to a random location.
* Make a background image.

## Takeaways
* I think referring to different codes seem to be the best way for me to learn. I will avoid plagiarism though through
writing comments to show my understanding of the code and, tweaking the code to fit my app.
