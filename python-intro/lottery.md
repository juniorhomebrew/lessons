---
title: Guessing the lottery
layout: lesson.html
---
##### ARRAYS, IF STATEMENTS, VARIABLES, RANDOM MODULE, DATA TYPES

This lesson, we will be using different data types and the random module to generate three random numbers. Then, IF statements will be used to check whether the numbers generated are the same as the user's inputs. An array will store the winning numbers.

![lottery](images/lottery.jpg)

## Task 1: Create the lottery machine
The national lottery has decided to scrap the idea of having a machine that spits out the winning numbers on balls due to the fact that there have been too many complaints of people having heart attacks due to the tension. You have been asked to create a machine that can come up with 6 random numbers. Then, it will ask the user to input 3 numbers, and if the numbers match, then we have a winner of £1,000,000!.

#### Step List:
* Import all the necessary modules; today we are using the random module

* Create an array to store our winning numbers
* Create a loop that will generate three numbers between 1 and 15; then store each number into the array.


#### Got lost? Here's the code.
```python
import random

# Creating lottery machine
# Create an array to store the winning numbers
lotteryMachine = []

# We need to generate 3 winning numbers.
# The best way to do repetitive things is with a loop.
for i in range(0,3):
    #generate a winning number between 1 and 20
    winningNumber = random.randint(1,20)

    #add that to our lottery machine
    lotteryMachine.append(winningNumber)
```

## Task 2: Taking User Inputs
Now that we have our machine with the winning numbers, it's time to take inputs from the user.

#### Step List:
* Create an array to store the user's inputs. We are creating an array because we are taking multiple inputs. Remember, an array is simply a basket that carries multiple variables

* Create a loop that will take three numbers from the user and adds each number into the array that we just created.


#### Got lost? Here's the code.
```python
# Taking the user's inputs

# Welcome message
print("Welcome to National Lottery Machine")

#we need to take multiple inputs from the user so it's best to store it in another array
#create that array
userInputs = []

#in a loop we will ask the user to enter their numbers
for i in range(0,3):
    #remember that python will take the input as a string, you must convert it to an integer
    numberEntered = int(input("Enter a number between 1 and 20: "))

    #add that to our userInputs array
    userInputs.append(numberEntered)
```

## Task 3: Check if Any Winning Numbers are Found
Now that we have the winning numbers and the user's guesses, we can check to see if the user has guessed the correct answers.

#### Step List:
* Start by creating a variable that will record the number of correct guesses

* Here comes the tricky bit. We need to take one of the user's inputs and check to see if it matches any one of the winning numbers. To do this, we will have to use what's called a **nested loop**, which basically means a FOR loop inside another FOR loop. The first loop will get each number one by one from the user input array; the loop within will check the number the user input against all the winning numbers. If there's a match then the number in the 'correct' variable will be increased by 1. It may be tricky but try drawing out what you want to happen before diving into the code.
* Finally, if the user gets all three guesses right, then the value in the correct variable should be 3, right? Well, then make an IF statement that only says that the user has won *if* all three numbers are guessed correctly. We don't want to tell the wrong person that they won a million pounds!

#### Got lost? Here's the code.
```python
### Check the number input against the winning numbers for a match

# We need a variable to keep track of the number of correct guesses the user makes
correct = 0

# We will be using a nested loop
# - which basically means a loop inside a loop

# Because we will be checking a number input against
# all the winning numbers for a match

for i in range(0,3):
    # Get the numbers input by the user one by one
    guess = userInputs[i]

    # This for loop will check the number that the user input against all the winning numbers
    for number in range(0,3):
        winNumber = lotteryMachine[number]

        # If a number matches then the number of correct guesses increases by 1
        if guess == winNumber:
            correct += 1

# If the user guess all three numbers, then tell them that they have won
if correct == 3:
    print("You have won £1,000,000!!!")
# Else, break them the bad news
else:
    print("Sorry but you did not win :(")
```
#### # What?
When you use a # in Python, the rest of that line is ignored by the computer. That's why we can write plain english afterwards, because the computer doesn't try to understand it as code!

If you add a comment, to remind yourself what the code does, use a comment! If you don't the computer will not be able to run your program, causing an **error**.

## And... we're done!
We've used multiple arrays and nested loops to create our national lottery machine. We used nested loops to check whether the user guessed the number correctly, and then we used an if statement to tell the user whether they had won or not. This is some pretty complex stuff. Well done!

## Challenge Task
If this wasn't hard enough then maybe you can go further!

* **Add validation**. What if the user enters a string (of characters, like a word or sentence) or a number that outside the range of numbers we are supposed to guess in?

* **What about second and third place**? Try to add in runner up prizes. If the user only guesses 2 numbers, then they get £5000, or if they only guess 1 number, then they get £1000.
