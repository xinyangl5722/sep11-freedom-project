# Tool Learning Log

## Tool: **Kaboom**

## Project: **Pixel Game (still planning)**

---

### 10/13/2024:
* I decided to dig deep into Kaboom since I didn't do that well of a research
	* I looked into the official website first
	* I first went into the playground and looked at some examples. I went into some sort of code where a sprite can move
	* I looked through examples. (I couldn't really find a way to tinker on jsbin because I need an image and I don't have one.)

### 10/18/2024:
* I first created a whole directory dedicate to tinkering my tool
* I decidded to learn how to get kaboom into my IDE
	* I went to the tutorial section of the official website
	* I first learned how to get the CDN into my IDE
	* I copied the CDN into my html
	* Now it's a grey and white checkered background

### 10/19/2024:
* I learned how to put a sprite inside my testing code.
	* I first grabbed a random transparent png photo and then put it in the directory
	* Then I added my sprite into my code
 ```js
const player = add([
	sprite("ghost"),   // sprite() component makes it render as a sprite
 	pos(120, 80),     // pos() component gives it position, also enables movement
])
```
* But when I looked at my sprite, it was too big

### 10/21/2024
* I learned how to move my sprites. i decided to use a different sprite which was the default green bean
	* I went to the playground first because the component tutorials are confusing
	* I saw the code on how they moved it so I put the codes for both arrows into my code so it kind of looks a lot like this.
```js
onKeyDown("left", () => {
	player.move(-SPEED, 0)
})
onKeyDown("right", () => {
	player.move(SPEED, 0)
})
onKeyDown("up", () => {
	player.move(0, -SPEED)
})
onKeyDown("down", () => {
	player.move(0, SPEED)
})
```
* So basically, if the left and right arrows are pressed, speed is at x axis. Negative is left and positive is right.
* If up and down arrows are pressed, speed is at y-axis. Negative is up and positive is down.


### 11/4/2024
* I basically learned how to do a dialogue
* I looked at the playground to see how they did it
* I made a box and made the code for the box.
* Then I created the dialogue which looks something like this-v
```js
const dialogs = [
        [ "bean", "Are you new here?" ],
        [ "bean", "I'm Qing Yao, but you can just call me YaoYao" ],
        [ "bean", "Oh yeah, we are in this Dream land. We are basically trapped in here and we have no choice but to go all through these levels or we will go to insanity."],
        [ "bean", "I need to pass the first three."],
        [ "bean", "Could you help me?"],
        ];
```
* I then started to recreate the code to make the text appear and changes when I press space-v
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
* Then I got my dialogue.

### 11/23/2024
* I learned how to make the sprite rotate
* I first looked in playground. Again.
* I went over to see the code that is responsible for making the sprite rotate
	* So I did that with my code
```js
player.onUpdate(() => {
	player.angle += 120 * dt()
})
```
* Then I was like "what if I just take the `dt()`?
* So I took that part out, and then the sprite was spinning really fast
* So then I looked at the 120, and see what happens if I turned it to 10
	* So this was how the code turned out
```js
player.onUpdate(() => {
	player.angle += 10
})
```
* The sprite went a lot slower so the number is saying how fast the sprite is rotating


### 12/8/2024
* Today I first decided to merge the content I had learned.
	* This pretty much means I'm putting the two concepts I learned together.
* So I had frist make the sprite rotate connect with the movement code so it kind of looks like this.
```js
player.onUpdate(() => {
	player.angle += 19 })

onKeyDown("left", () => {
       player.move(-SPEED, 0)
})
onKeyDown("right", () => {
       player.move(SPEED, 0)
})
onKeyDown("up", () => {
       player.move(0, -SPEED)
})
onKeyDown("down", () => {
       player.move(0, SPEED)
})
```
* So now my sprite is turning while moving

### 1/1/2025
* So today, I decided to change the background because I don't want the grey checkered background anymore
* I found this [video](https://www.youtube.com/watch?v=l6cwmwW40jw) on how to make a shooting game so maybe I can use that as inspiration for changing the background
* So I found out that he made his screen pitch black so that could be the first step to my game because I still need to find out how to make sprites and stuff
* So I did the code to change the background to pitch black, and it looks like this
```
kaboom({
	background: [0, 0, 0],
	scale: 0.5,
        });
```
* Kaboom uses RGB color hex, so I used 0,0,0 for it and made a scale for it, but then my sprite was gone.
* So then I decided to delete the scale and see what would happen
```
kaboom({
	background: [0, 0, 0],
        });
```
* And when I run the code again, the sprites finally popped up!


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
