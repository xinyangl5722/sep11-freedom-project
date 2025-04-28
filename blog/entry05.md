# Entry 5
##### 4/24/2025

## Creating the Minimal Viable Product (MVP)
So I did not really follow my [plan](https://github.com/xinyangl5722/sep11-freedom-project/blob/main/prep/plan.md)had a few hard times on making my mvp. I started off with creating a start scene and then adding a text for the scene. Then I decided to add another scene for a dialogue. I started to create another scene for the game. I had a hard time connecting these together. I later put them inside an if-statement that is in a function.
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

### EDP
I'm currently somewhat finished with **Create the prototype** and also finishing **testing the prototype**. I created the minimum for the project. However, I have also tested it by going through the game. However, I still need to continue improving the game by adding a few more levels and improving the text.

### Skills
One skill I have learned is **Attention to detail**. During my code, I had a lot of errors while creating the mvp. Many of these errors were syntax errors. I was able to learn how to fix the errors and spelling the code correctly.
Another skill I have learn was **Debugging**. Many of these errors was also about debugging code. Sometimes, I forgot to define a variable in the game, and sometimes, I might have created an error in writing a variable for the other one. So I learned to debug it by putting the variables in the same place in order for the code to work.

### Summary
In short, I have made some progress in creating my mvp. Now all I need is to create my beyond mvp where I create more levels and fix the textbox in my dialogue scenes.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
