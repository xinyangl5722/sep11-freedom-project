# Entry 4
##### 3/10/2025

## Tinkering Process Part 3
I also had gotten little progress over the days as well. However, I got the process of making an obstacle course. Some part of the main obstacle course is that there has to be a platform surface in every obby game or else you will be falling in the air. So I decided to make something for my green bean sprite to land on. First, I created some sort of layout for the obstacle course.
```js
const level = addLevel([
  "  @    ",
  "=======",
],
```
Then, I assign each symbol a sprite. I decided to make the _@_ symbol for the green bean sprite. However, since I don't have the sprite for a flat surface, I decided to just use the boy sprite. Later, I decided to make the boy a solid surface, which is to make it static. 
```js
"=": () => [
  sprite("boy"),
  area(),
  scale(0.1),
  body({ isStatic: true }),
  anchor("bot"),
],
```
The `body({ isStatic: true })` shows that the player would stay on top of the boy sprite like standing on the stool. Later, I decided to make the green bean sprite jump and move left and right. Howevedr, my main goal is for the green bean to jump. So this is what I did.
```js
onKeyPress("space", () => {
  if (player.isGrounded()) {
    player.jump()
  }
})
```
This code means when when press the space bar and the player is on the ground, it will jump. So then after making this code, my sprite can now jump when the space bar is pressed. I also decided to make the camera focused on the green bean sprite. This is pretty much common in obstacle games so I decided to do that. So I created this code.
```js
player.onUpdate(() => {
 camPos(player.pos)
})
```
So now, my camera is focused on the green bean sprite. The camera is a bit shaky. Probably it's because my green bean sprite is on a boy sprite instead of a block sprite.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
