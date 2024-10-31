# Entry 1
##### 10/28/2024

## Deciding and Tinkering My Tool
I had recently decided on what the topic of my freedom project is going to be. To sum it up, it is an interactive pixel story game. This is only the base of my idea so I may need to think about it a bit more. While I had put that aside, I had picked out my tool for my project. The tool is called **Kaboom**. I decided to tinker with this tool because of how my aspects of this game fits in this tool.
I first researched Kaboom on the [official website](https://kaboomjs.com/).   
I first went to the [playground](https://kaboomjs.com/play?example=add) to see how each code works for different components. Then I started to look at the code to see how it works. I basically installed kaboom into my code for testing and learning my tool and I used the code in the playground inside my testing section. So basically one of the first components I did was making a sprite move. So I basically did this.
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

## EDP
I have already defined my problem, and brainstormed a possible solution, so now I am **planning the solution**. I am currently planning my game and planning on what to use with my tool. I am still currently in the stage of planning my solution as I still need to figure out the sequence of my game and the components I need for kaboom to make my game.

## Skills
One of the skills I have learned was **How to learn**. When I started to tinker my code, instead of looking over multiple video tutorials that are like 4 hours long, I used playground to see the codes they used to see how it works. One of them was adding a sprite. I followed the playground code to see how it works and I encorporated it into my own code while testing it.
```js
const player = add([
	sprite("ghost"),   // sprite() component makes it render as a sprite
 	pos(120, 80),     // pos() component gives it position, also enables movement
])
```
Another skill I have learned was **creativity**. I have learned how to be creative with my game and plan on what my game should be like such as backgrounds, the genre and concept of the game, etc. For my game, it was based off of a random universe I had created inside my head. I turned my characters in this universe to be in a small pixel game where they have different levels in a world where they were the only inhabitants.

## Summary
So in short, I had decided about what tool I decided to use and I had tinkered with it for some time. I had also come up with a plan about my project and how I planned to do a pixel game about one of mu universes I had created for them. Overall, I am still looking foward to tinker my tool and plan my game in detail.


[Next](entry02.md)

[Home](../README.md)
