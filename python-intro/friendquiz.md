---
title: Who Knows Me Best?
layout: lesson.html
---
##### VARIABLES, INPUTS, OUTPUTS and BOOLEAN
Have you ever wanted to see which of your friends know the most about you? Well, you could easily do this by asking your friend questions and checking if their answers are correct. But asking them in person is *sooooo* 2015.

We could make this faster with a simple piece of code! If we use what we know about variables, to store the answers; and use **inputs**, to take your friends' answers to questions; we can print out if they got the questions right or wrong!

## Task 1: Printing
When the user answers the questions we would want to tell them if they got it right or wrong. To do this we will need a way of showing something on the screen so they can read if they got it correct or incorrect. In computer science, we call this an **output**. That's because the computer program **outputs** something, for the user to see. This task will should you how it's done.

#### Step List:
* Get your code editor open and ready!
* Start the first line right at the beginning of the first line (not spaces or indents before the text).
	* Since we're using Python, we have to do this otherwise the program will get confused. Spaces and indents at the beginning of a line can only be used for some cases, but we'll get onto that later.
* Type: `print("I like to code! ")`.
	* Make sure that the first bracket is touching the word `print`, otherwise it won't work!
	* Don't forget to use apostrophies or speech marks around "I like to code!". We have to use them because `I like to code!` is a sentence, rather than a variable, which is what we'll get onto in a minute.
* Run your program!
	* What did you see? If everything went well, the sentence "I like to code!" should be printed (or outputted) to you!
	* Your code should look like this:
​``print("I like to code!")``
	* In our piece of code we will be outputting if the user's answer matches the correct answer. We will talk about how to do this later!

## Task 2: Remember variables?
When we are setting the answers for your questions we need to store them in things called variables; hopefully you've seen these before, but here's a little reminder. Computers don't automatically remember things, instead we have to store these things so we can use them later. In this case, we need to store the answers so we can use them to check if the user's answer is same as the correct answer.

#### Step List:
* Make a variable with a number value, using ``Age = 11``
	* A variable is a way of storing a value. In this case, we'll store an integer value.
	* Using the equals sign, **assigns** a value to the variable. This is done so that we can **refer** to it later.
	* You should read it as "Age refers to 11". That's how we assign things.
	* An integer is a whole number, this means that it cannot be a fraction or a decimal.
* ``EyeColour = "brown"``
	* This is how we give a variable a value.
	* In front of the equals, there is the variable name. This doesn't need speech marks.
		* Variable names must start with a letter, and can only include the alphabet, numbers and underscores.
	* The equals says that the left is the same as the value of the right. This way, everytime we say ``EyeColour`` in the rest of the program, it's the same as saying ``"brown"``.
* Try making a variable called ``PetName``, and give it the name of your pet.
* Now try printing the variable.
	* Remember that we don't need speech marks!
	* See what it printed out!

#### Got lost? Here's the code.
```python
PetName = "Kittens"
​
print(PetName)
```
  Why do we use variables? The clue is in the name. If we need to use the pet's name a hundred different times in a long program and we decide to change it, then we will have to go to one hundred different places to do so.
  ​
  With a variable, **we just have to change the value in one place**, and then everywhere else the value changes. We can vary what the value is. We can also change the value of it half way through a program.

## Task 3: Ask the user
To check if your friend knows a lot about you, you will need to ask them questions. In our piece of code we will need to remember (store) the user's answer and check if it's the same as the answer you already stored before.
  ​
#### Step List:
  * Make a new variable that has nothing assigned to it.
  	* Same as before. For example: ``name = ``
  * Change that variable's value (the part of the right), to be ``input()``.
  	* It's very important to have the brackets touching the word input, otherwise the code won't work!
  	* When the user answers in the box, they don't need to put speech marks around what they type. The computer does this automatically when you use ``input()``.
  * Run this code.
  	* The program should come up with a little input box.
  * Change your code to print the variable.

Your code should look like:

```python
name = input()
​
print(name)
```

  The user doesn't know what to input unless they read the code! Let's make the pop-up box ask the user a question.

  * Put your question inside the brackets of ``input()``, but remember the speech marks!
  	* Speech marks will be needed as we are using words, not variables in our question.
  * We can print multiple things in one go by using a comma in the print function.
  	* The comma can't be in speech marks! We are not using it as a comma, but as a separator.
  * Try printing ``"Your name is"`` before the ``name`` variable is printed.
  ​
#### Got lost? Here's the code.
```python
name = input("What is your name?")
​
print("Your name is", name)
```
  ​
By using inputs the user can interact with the program. We can use variables with them, so that the user can change what the program does. If we didn't use variables, the user would have to go into the code and modify it to print their name.
  ​
  Using a variable means that we only have to ask the user once, and the values are changed everywhere!

## Task 4: Making the true-friend test
Now that we know how to get the user to input something and store that to a variable, we can check if the user's answer is the same as the answer stored. We will do this by using something called **boolean**. Boolean just means that the final value can either be true or false. That's it!

We get a boolean value when we compare 2 values to check if they are equal to each other. To compare two values we use double equals sign like this, ``==`` (this is different from just ``=``, which assigns variables).

#### Step List:
* Make a new variable called ``favouriteFood `` and set it to equal your favourite food.
	* Same as before. For example: ``favouriteFood = "pizza"``
		* Remember to use quotation marks around the word on the right side.
* Then type: ``print(favouriteFood == "pizza")``.
	* Remember to use a double equal sign to compare the two values.
	* In this case, we are comparing the value stored in the 'favouriteFood' variable, to the string (that's a series of characters), "pizza".
* Run this code.
	* The program should print the word ``true``.
	* This is because the value of ``favouriteFood `` is equal to the value of ``"pizza"``.
* Now change the value of the variable``favouriteFood `` and see what is outputted.

#### Got lost? Here's the code.
```python
favouriteFood = "pizza"
  ​
print(favouriteFood == "pizza")
```
  ​In our code we can use **boolean** to check if the user's answer is equal to the answer that has been previously been set!

## What we've learnt so far...

We've used **variables, inputs, outputs** and **boolean** to try to see which of your friends knows most about you.

* We learnt that **outputing** is when you display something from your code on the screen and we do this by typing: ``print()``
* We also learnt that we use **variables** to store things in our program and that they are useful because we just have to change the value in one place for the value to change everywhere else.
* In addition, we learnt that **inputs** are used so the user can interact with the program. We do this by typing: ``input()`` and making sure the brackets touch the word 'input'.
* Finally, we learnt that we use **boolean** to compare two values, and that the outcome will always be true or false.  To compare two values we use double equals sign like this, ``==``.
​

## Task 5: Asking multiple questions
Now we can use all these new skills to make a piece of code that checks if the user knows you well! We can put lots of code together, and make the computer run it all. The computer reads like we do: down the page. This means that each line is run after the one above it.

Here is a simple example I made earlier.

```python
age = 11   # The correct answer is 11

UserAnswer_age = int(input("What is my age? ")) # User asked

print (age == UserAnswer_age)

food = "hot dog"
UserAnswer_name = input("What is my favourite food?")

print(name == UserAnswer_name)

EyeColour = "brown"  # Correct answer for eye colour stored
UserAnswer_EyeColour = input("What is the colour of my eyes? ")

print(EyeColour== UserAnswer_EyeColour)
```
##### Line by line explanation
1. Sets the variable ``age`` to the value 11.
	* It is stored as an integer automatically, not a string!
2.
3. Asks the user (your friend), "What is my age?".
	* Their response is stored as a **string**, so we have to convert it to an integer so that we can compare it (confused? Read below).
4. blank line
5. We compare the correct answer to the user's answer using the ``==`` operator. If they are the same, then the statement ``age == UserAnswer_age`` is ``True``. If not, then it is ``False``. The outcome of the comparison will be printed.
6.
7. The correct answer ``"hot dog`` is stored in the variable food. We used the ``=`` assignment operator here, rather than the ``==``, which makes a comparison.
8. The user is asked what your favourite food is, and their answer is stored in the variable ``UserAnswer_name``.
	* We didn't have to convert it to an integer here, because the correct answer is a string, and the input() function gives us a string too.
9.  
10. A comparison of answers is made again with our **Boolean operators**. Remeber that **Boolean** means that the outcome can either be *True* or *False*, nothing else!
11.
12. The correct answer is again stored, but this **assignment** is followed by a comment, using ``#``. Hopefully you know what these do! (Hint: everything after the ``#`` on a line is ignored by the computer)
13. The user is asked for their response again.
	* Just to note: you can name a variable whatever you like (as long as it is only numbers, letters, and underscores. It also can't start with a number). We chose to user ``UserAnswer_x``, because it's easy to understand what we stored in the variable. Good, sensible names are important to make you code easy to read!
14.
15. A final **Boolean** comparison is made, printing either True or False to the screen.

##### int()
In one point in the code, we have ``int(input("What is my age"))``. The user will hopefully enter a number. Using ``int()`` allows us to convert whatever the user entered into a number. Even if the user enters ``12``, it will still have to be converted.

This is because no matter what the user enters, it will be treated as if it were a word. But the answer is an integer (a number without a decimal point); so we convert the answer to an integer, so that we can compare the value to the answer.

Even if a string (such as ``"12"``) and an integer (such as ``12``) look the same on the inside, they're not! One is number, and the other a word, so every time that we compare them, no matter what they are on the inside, they are not going to be the same.

If you try to convert a string that is not numbers, you'll get an error, and your code will stop working. It's pretty obvious that you can't make ``"sausage"`` into a number! Try it!


## Challenge Task
Now that we have finished the last task, lets try something a bit more challenging! Let's adapt this program so that it displays the correct answer to question when the user gets the question wrong and congratulates the user when they get the answer right.

* HINT: You may have to use **if and elseif statements** as well as **boolean operators**. (Double hint: have a Google if you don't know what if statements are! Google is a programmer's best friend!)
