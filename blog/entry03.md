# Entry 3
##### 1/3/2025

## Tinkering Process Part 2
I recently had made little progress, but I did achieved one thing from my winter break goal. I recently had learned how to make my sprite collect an item, and changing the background. This is a great essential to my game as the main goal for the game is to make the character collect items in order to move on to level by level.
First, I learned how to change the background. I didn't want the background to have the same checkered grey squares and wanted to change the color of the background instead. I looked at a [YouTube tutorial](https://www.youtube.com/watch?v=l6cwmwW40j) and there was a moment on where the person changed the background to black. So I did this code.
``` js
kaboom({
	background: [0, 0, 0],
    });
```
The three 0s represents the color black, so when I look back at my website, the background is now pitch black.
Now I wanted my sprite to collect items which is a major part of my game. So I looked at the [Kaboom Playground](https://kaboomjs.com/play?example=rpg) to figure out how to make my sprite collect things. I later figured out how to. I figured out the `.onCollide` code so I tried it out and this was what I got.
```js
    player.onCollide("enemy", (enemy) => {
        destroy(enemy)
        })
```
I also added another sprite that I categorized as "enemy". So now when I move my sprite closer to the item, it disappeared.
That is what I have so far, but I wanted to figure out how to add scenes into the game as well as backgrounds. bv

## EDP
I however, am still at the **planning the solution** step as I still have a long way to go to complete all the learning aspects I need to make the code. I have finished a few parts of it such as changing the background color and collecting items. So, I still have mores stuff to learn, but hopefully, I will be able to get there.

## Skills
One of the skills I believe I have developed was **How to learn**. I looked over the code that leads to the certain result in the outcome to understand how it works. For example, I have learned what `.onCollide` represents as when I looked at the code, it looks like a function. the `.onCollide` would mean that when one thing collides with another.
Another one of the skills I believe I have learned was **How to google**. Technically, I did some digging on YouTube. I looked over tutorials that could benefit me in changing my background by typing something like "how to change background color on kaboom". I found a [video](https://www.youtube.com/watch?v=l6cwmwW40jw) on how to make some sort of game which I believe it has some of the components I would need to create my game. So I looked into that and found out how to change my background color.

## Summary
In short, I did some sort of progress, but I am hoping to get a bit more progress on learning the aspects of _Kaboom_, starting on how to make different levels.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
