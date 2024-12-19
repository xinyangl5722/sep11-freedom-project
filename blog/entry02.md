# Entry 2
##### 12/9/2024

## Tinkering Process Part 1
I recently learned a bit of the concepts of sprites. This means I learned how to rotate a sprite, give it dialogue. First, I learned how to create a dialouge. I started with this code.
```js
const dialogs = [
        [ "bean", "Are you new here?" ],
        [ "bean", "I'm Qing Yao, but you can just call me YaoYao" ],
        [ "bean", "Oh yeah, we are in this Dream land. We are basically trapped in here and we have no choice but to go all through these levels or we will go to insanity."],
        [ "bean", "I need to pass the first three."],
        [ "bean", "Could you help me?"],
        ];
```
I first used `const dialogs` for the dialogues. Then I used square brackets. The first quotation show the sprite representing that sprite is talking, so bean is talking. The next quotation show what bean is saying. Then, I made a code that go to each dialogue every time the space bar is pressed. So I did this.
```js
onKeyPress("space", () => {
            // Cycle through the dialogs
            curDialog = (curDialog + 1) % dialogs.length
            updateDialog()
        })

        function updateDialog() {
            const [ char, dialog ] = dialogs[curDialog]
            // Use a new sprite component to replace the old one
            avatar.use(sprite(char))
            // Update the dialog text
            txt.text = dialog
        }

        updateDialog()
```
For this code, I made the dialogue to the next dialogue after each space press.

Next up, I decided to spin my sprite. I started off with this code.
```js
player.onUpdate(() => {
    player.angle += 19 * dt()})
```
The play angle shows how fast the sprite rotates. I wonderr what happens if the `dt` is deleted. So I deleted the `dt` and it made my sprite rotate faster.  
Currently, this is pretty much what I have so far, but when the winter break ends, my goal is to figure out how to add a background into the game so it doesn't look like the default checkered square that I currently have. I also wanted a character to interact with a sprite that will be an item such as picking up the item when you click on it. Plus, I also wanted an interaction between the main sprite and the enemy sprite such as the enemy sprite chasing the main sprite around until it catches the main sprite. But my actual goal is to complete at least two of these aspects to be learned.

## EDP
I am currently still on **Planning the solution**. I am still working on how my knowledge of using kaboom will turn my results to and I still need to see which components I need to do. I may also need to figure out how I can put different scenes together since I have a lot, but I think I'll start with something small.

## Skills
One of the skills that I developed is **How to learn**. I looked over the [official website](https://kaboomjs.com/) and looked over tutorials and looked at the comments in the playground to see how they worked. For example, I learned how to rotate a sprite using this code.
```js
player.onUpdate(() => {
    player.angle += 19 })
```
I figured out what the `.onUpdate` and `.angle` meaning by looking at the comments as I learned that `.onUpdate` means it registers the event every frame and `.angle` is basically the speed of the rotation at the number of seconds and for this code, 19 degrees per second.

Another skill I had developed still is **creativity**. I can figure out what I can do with the code I had learned from the tool I created. For example, the rotating sprites can be for rotating objects being waited to be found. The dialogue codes can be used for the beginning and the end with my character.

## Summary
In short, I still believe I have a lot to learn about my code and how it will work on my potential game. I am planning to start encorporating my own pixel character and learning how to make backgrounds.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
