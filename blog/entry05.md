# Entry 5
##### 4/24/2025

## Creating the Minimal Viable Product (MVP)
So I had a few hard times on making my mvp. I started off with creating a start scene and then adding a text for the scene. Then I decided to add another scene for a dialogue. I started to create another scene for the game. I had a hard time connecting these together. I later put them inside an if-statement that is in a function.
```js
onKeyPress("space", () => {
    // Cycle through the dialogs
    curDialog++
    if(curDialog < dialogs.length){
        updateDialog()
    }
    else{
        go("game2")
    }
})
```
So I first made a function for when the space is pressed, the `curDialog++` which is which dialog it is in. It says that if the curDialog is greater than the amount of dialogs in the array I just made, it will go to the next scene which is my next game scene `game2`.
Then, I had some time drawing my pixel adjustments because sometimes I drew them too small and there will be gaps that take up literally the majority of the space. Later, I created the code for the pixel character to move the key by using `isStatic: true` and then create another code when it touches the door sprite I made.
```js
Key.onCollide("door", () => {
    go("game3")
})
```
So the `Key.onCollide` is if the key sprite collided onto... and the key sprite is colliding to the door sprite. So if the key sprite touched the door sprite, it will go to the third scene which is another game scene `game3`. [This is currently my game so far.](https://xinyangl5722.github.io/sep11-freedom-project/index.html)
So as I'm writing this, the game is still not done. I am having trouble making the block sprite completely still since my pixel will fall in the middle of each block sprite when it jumps.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
