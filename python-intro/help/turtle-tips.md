# Basic Python Turtle Commands
You can use Python and Turtle on our site (using Google Chrome works best):
[**hbrew.club/onlinepython**](http://hbrew.club/onlinepython)

| Python Function   | Example         | What does it do?                                               |
|-------------------|-----------------|----------------------------------------------------------------|
| forward(spaces)   | forward(10)     | Moves forward                                                  |
| backward(spaces)  | backwards(10)   | Moves backwards                                                |
| right(degrees)    | right(20)       | Turns right (clockwise), on the spot                           |
| left(degrees)     | left(90)        | Turns left (anticlockwise), on the spot                        |
| goto(x, y)        | goto(20, 60)    | Goes to the given position                                     |
| speed(s)          | speed(10)       | Changes the drawing speed                                      |
| circle(radius)    | circle(5)       | Draws a circle                                                 |
| dot(size, colour) | dot(2, "black") | Draws a dot                                                    |
| undo()            | undo()          | Undoes the last movement                                       |
| position()        | position()      | Gives the current co-ordinates of the turtle                   |
| penup()           | penup()         | Lifts the pen up (so you can move around without drawing)      |
| pendown()         | pendown()       | Puts the pen back down                                         |
| pensize(width)    | pensize(4)      | Changes the width of the pen                                   |
| color(c)          | color("blue")   | Changes the colour of the pen (remember the American spelling) |

This is only a set of the most basic functions, thereare lots more to try out, and there are more settings for many. Look at the full list at [https://docs.python.org/3.2/library/turtle.html](https://docs.python.org/3.2/library/turtle.html).

## Remember to add t. before the function, here's an example:
    import turtle           # Import the turtle library
    
    t = turtle.Turtle()     # Make a turtle (you need one)
    t.forward(10)           # Move the turtle forwards 10

Sometimes, the turtle goes off the page. You can change the size of the canvas (the part where the turtle draws on) using: 

    height = 600        # The max canvas size is shown in the top
    width = 500         # right of the online Python output
    
    screen = turtle.Screen().setup(width, height)
