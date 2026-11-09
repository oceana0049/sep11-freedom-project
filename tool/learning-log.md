# Tool Learning Log

## Tool: **Kaboom**

## Project: **Freedom project**

---

### 10/25/26:
* learned about the 3 functions, kaboom(), add([]), and loadSprite()

* add() puts something into your game
onKeyDown does an action when you hold a key
onKeyPress does an action when you press a key
onCollide does an action upon colliding

* I had extreme difficulty with tinkering as all the good websites were either blocked, or taken over by AI. 

<!-- 
youtube.com
-->

### 11/8/26:
* coded some basic kaboom and followed the official tutorial.

THINGS I LEARNED:
* components give an object a certain functionality, like human limbs.
* "add" meshes the components together to make a functioning object.
* pos gives a sprite a screen position, area allows it to be detected when it collides with another object, body allows it to fall and jump/
* rect creates a rectangle, which gives it a height of 48 and a width of whatever width is. outline creates an outline of 4 pixels. body isstatic: true makes the object not move, and forces all onjects to stop when touching it. color simply gives it a color, determined by a numerical code.

* CODE SNIPPETS (This code is not mine, i typed it out using the kaboom tutorial.)

* Loading kaboom and the sprite
kaboom()
loadSprite("bean", "sprites/bean.png")

* Loading the bean sprite, and allowing it to jump:
const bean = add([
	sprite("bean"),
	pos(80, 40),
	area(),
	body(),
	])
onKeyPress ("space", () => {
	bean.jump()
})

* Adding the ground:
add([
	rect(width(), 48),
	pos(0, height() - 48),
	outline(4),
	area(),
	body({ isStatic: true }),
	color(127, 200, 255),
])

* Setting the gravity:
setGravity(1600)

* Now, we have a bean that falls and hits a floor, and can jump.