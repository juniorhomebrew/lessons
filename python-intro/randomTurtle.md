---
title: Randomly Walking Turtle
layout: lesson.html
---
##### MODULES, WHILE, BOOLEAN
In this lesson you will be using a **module** called Python Turtle. I know what you're thinking, what's a **module**?! Well, a **module** is a block of code (usually a block of code that is hard to code yourself) that somebody has already coded for you, so all you have to do is import it and save yourself lots of coding time! Every module does a different thing - this module (Python Turtle) allows you to draw shapes using a turtle that draws lines. Today, we will be using Python Turtle to draw a random path for the **Turtle** to follow until it gets back to its starting point. In order to do this, we are going to need another module called **random**.
## Task 1: Setting the turtle up
<!-- Break into paragraphs -->
The first thing that we need to do is get the turtle module ready. For this lesson, you won't be using portable python - you will instead be using an online python emulator made for running turtle!

<!-- Steps and reasons for doing it -->
#### Step list:
* Open up your web browser of choice.
* Go to this link: http://hbrew.club/onlinepython/index.html
	* This link will take you to the online python editor
	* Underneath `import turtle`, Type: `import random`
* Delete all code underneath the line `t.color("white")`

You are now ready to start using the Python Turtle!

## Task 2: Finding a Start point
<!-- Break into paragraphs -->
Now that the turtle is set up, we need to define a start point for the turtle.

<!-- Steps and reasons for doing it -->
#### Step list:
* Return to the webpage you modified in **Task 1**.
*  Underneath your current code type: `h = t.pos()`
	* This line of code is assigning the current co-ordinates of the turtle to the variable `h`.
* On a new line type: `t.fd(1)`
	* This line of code moves the turtle forward by one unit.

You now have the co-ordinates of the starting point of the turtle and have moved the turtle forward by one.

## Task 3: Creating a random path
<!-- Break into paragraphs -->
Now that you have the starting point of your turtle you can now code a **while** loop. This while loop would move the turtle at a random angle for a random distance **so long as** the current position of the turtle is not equal to the starting position of the turtle you defined in **Task 2**.

<!-- Steps and reasons for doing it -->
#### Step List: 
* Return to the webpage you modified in **Task 1** and **Task 2**.
* On a new line, type: `t.speed(100)`
	* This line makes the turtle move at a speed of 100, but you can change the speed to whatever number you like!
* On a new line, type: `while t.pos() != h:`
	* Make sure you add the colon on the end of this line!
	* This line of code continuously runs the block of code underneath it, so long as the current position of the turtle is not equal to `h`, the starting position of the turtle.
* On a new line (indented), type: `t.lt(random.randint(1,360))`
	* This line of code in the while statement rotates the turtle left to a random degree between 1 and 360.
* On a new line (indented), type: `t.fd(random.randint(1, 5))`
	* This line of code moves the turtle forward between 1 and 5 units.
* Run the code!

Your code should look like this:
```
import turtle
import random

t = turtle.Turtle()
t.color("white")

h = t.pos()
t.speed(500)
t.fd(1)

while t.pos() != h:
	t.lt(random.randint(1,360))
	t.fd(random.randint(1,5))
```
Once you run the code you will see the turtle randomly moving around the screen in different directions. If you see this, congratulations! You have created a randomly walking turtle!


##Challenge Task: Red, White and Blue
<!-- Break into paragraphs -->
If you are reading this you have probably finished the main three tasks and are seeking a challenge. well, you've come to the right place! Your challenge today is to make your turtle randomly switch colors between red, white and blue every time it moves!

**HINT:** create an array with the three colors and **randomly** index the array in the **while** loop. 

