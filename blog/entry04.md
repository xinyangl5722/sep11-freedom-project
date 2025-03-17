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

### EDP
I'm still at the **planning the solution**, but I'm getting closer to **making the prototype**. I firgured out the main compartments for an obstacle course currently. However, I still need to figure out how to create scenes for each part of the game. I still have a lot of stuff to learn but I think I will be getting there.

### Skills
One skill I have developed was **creatiivity**. I learned to create new ideas for my game in the second level and decided to make an obby instead. I also developed my skill of **how to learn**. I learned how to make the basics of an obby such as making a sprite being solid which can be on top of using the `isStatic: true` code. In addition, I had also learned to make the camera focused onto the main sprite going to the obstacle course by using the `camPos` and using the `player.pos` to focus on the player.

### Summary
In short, I created the basics for an obstacle course. I made the camera focusing onto the player, and I created a basic platform for the player to just walk and jump around on. Next step is to find out how to create a scene and connecting those one by one.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
