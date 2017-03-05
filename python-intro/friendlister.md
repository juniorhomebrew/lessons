---
title: FaceArray
layout: lesson.html
---
##### ARRAYS, FOR LOOPS
Facebook is getting old (plus you can't use it until you're 13)! We need a better way to store our friends, and we will be writing the code to make sure that it's safe!

![Facebook? No!](images/facebook.jpg)

By the end of the lesson you will feel confident using loops in Python, in particular, **FOR loops**. These will allow you to repeat lines of code over and over again!

After you've got this sorted, there won't be any need to copy and paste code again!

Arrays will be re-introduced and used again, to help you learn about **data structures** in more detail, and how we can use them in loops! All of this will be done using skills you already have, such as inputs and outputs to create some snazzy new code!

## Task 1: Array and user inputs reminder!
You can probably make a mental list of some of your best friends, but sometimes hey can get hard to remember (especially when you're as popular as you are).

Do you think we can use some **data structures** to help you digitalise this list? How about entering data? Let's start with making an array, and asking the user for some data!

#### Step List:
* Create an empty **array** (or list). It will hold a list of your best friends, so make the variable appropriate!
* Assign a best friend variable to the user input asking who your *best-est* friend is.

Simple enough? If you think you can manage it, put the input into the array (hint: you have to ``append`` it).

#### Got lost? Here's the code.
```python
# An empty array that will shortly contain your friends
BFArray = []

# Asking the user for their best friend
BestFriend = input("Who is your best friend?")

# We don't do anything with the information yet!
```

##### What's going on?!
An empty array is created that will act as a placeholder for friends to be added further on. We assign it to a variable, so that we can keep track of it, and modify it later on.

Keeping **variable assignment** at the top is considered standard. It means we can see what is used in the program, all in one place, and that the computer won't have a hard time finding it!

A user input asking for the user's best friend is assigned to its own variable being `BestFriend`. Did you manage to put the input into the array?
​
## Task 2: FOR loops
You have more than one friend, right? So we are going to want to ask 'Name your friend' or something along those lines more than once, this is where for loops will allow us to execute lines of code multiple times, this will save time and allow for easier editing of your code if something needs changing in the future.

Now we have a few names of friends, but what are we doing with these values? We created an empty array earlier that acts as a simple list meaning we can add all of the friends into the array. The names in the array can then be printed very simply in a short amount of code later.
​
#### Step List:
* Use a for loop in whatever appropriate range to ask for the user input of the next friend and add it onto the end of the array using the append function, 3 or 4 friends keeps it practical, remember python starts counting at 0 and stops counting the number before the one that is put down e.g. 'for i in range (0,4)' will run 4 times.

#### Don't just copy this! Here's some help.
```python
for i in range (0,4): # A for loop will run 4 times
    Friend = input("Who is your next favourite friend?")
    # This question will be asked however many times the range is for and retrieves the user input to then put in the list
    BFArray.append(Friend)
    # The append function puts the value at the end of the array by default, this is fine for our needs
```

##### What's happening here?
A **FOR** loop is executed in this example 4 times – ***i*** is a  variable that is used to count the through the loop.

Inside of the loop a variable labeled 'Friend' is assigned to the user input that the user enters. We'll use this variable, Friend, to contain someones name.

The next line uses the append function to put this new friend value into the array. This is done by the `array.append(value)`.

**NOTE:** This is then repeated with a new variable for Friend when the user enters a new user input and is put on the end of the array!

## Task 3: Best friends - Using different functions within for loops
Now we have an array that contains a list of best friends but does not contain the very best friend. No worries here as this was stored in its own variable.

We are going to want to print this first as otherwise the friends that come afterwards would be seen as better friends than your best friend as they would be printed first. We are going to use another for loop in order to print the friends but in a slightly different way.

#### Step List:
* Print out your best friend as this one is not in the array although could quite easily be implemented to be put at the front of the array

* Use another for loop which will go through the array and print each index out. However (0,4) should not be used as if we wanted to change the amount of times the user input is asked it would mean that remembering to change the range here would be necessary as well. As we want it to print out the array the range only has to be the length of the array. This can be done using (len(array)) as the range

#### Got lost? Here's the code.
```python
print (BestFriend) # The best friend is not in the array and although it could be I have a simple print statement above the repeating print loop so that the best friend is shown first

# Here, we create a range of numbers
for i in range(len(BFArray)): # len() gets the amount of items in the array
    # It's the "length"

    # Print the best friend at index i
    print (BFArray[i])
```
**REMEMBER:** It's really important that you **indent** your code, since this is the code that will be repeated! If the code isn't indented, the computer doesn't know

The first line simply **prints** the best friend variable which will contain the name that the user first entered when the 2nd line of code ran.

This line is above the for loop as the list of names need to go from best friend to least best friend.

Finally another for loop is used however the range is determined by the length of the array rather than a hardcoded integer which means that the loop will not accidentally run not enough times or attempt print a variable from the array in a position that does not exist i.e. index 4 (the 5th value in the array) would not exist and having it run in this range would cause errors that can easily be avoided. The code inside the for loop simply uses the same hypothetical i to count through the index printing each name inside of the variable!

#### Why is index 4 the 5th value?
Because computers count from 0 upwards, so the first value is at index 0!

## And... we're done! Here's a challenge!
We are now capable of asking the user for their own input, this is an incredibly useful skill as it allows people to interact with the application or game in order to personalise it and make it more entertaining!

We can now create an array which is known as a form of 'data structure' in order to store information to then be used later on, this is valuable as for complex programs vast amounts of data need storing and organising to then be able to access it later on and manipulate.

Finally we used for loops in order to shorten our code and repeat lines of code a chosen amount of times without having to manually copy and paste it. Loops becomes incredibly powerful later on when paired with things such as conditional statements and this shows professionalism in your code!
