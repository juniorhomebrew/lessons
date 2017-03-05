---
title: Auto-Author
layout: lesson.html
---
##### VARIABLES, INPUTS and OUTPUTS

Writing stories can take a long time! What if we started off with a story, and then just had to put in the details? If you've every played consequences, this is very similar: we ask the user for the name, activity etc. and then we take what they gave us, and make it into a beautiful, and often ridiculous story!

## Task 1: Showing some text on the screen
There's no point in making a story if no one can see it, so we need a way to show everyone what's going on. In computer science, we call this an **output**. That's because the computer program **outputs** something, for the user to see. This task will should you how it's done.

#### Step List:
* Get your code editor open and ready!
* Start the first line right at the beginning of the first line (not spaces or indents before the text).
	* Since we're using Python, we have to do this otherwise the program will get confused. Spaces and indents at the beginning of a line can only be used for some cases, but we'll get onto that later.
* Type: `print("Hello World!")`.
	* Make sure that the first bracket is touching the word `print`, otherwise it won't work!
	* Don't forget to use apostrophies or speech marks around "Hello World". We have to use them because `Hello World!` is a sentence, rather than a variable, which is what we'll get onto in a minute.
* Run your program!
	* What did you see? If everything went well, the sentence "Hello World!" should be printed (or outputted) to you!
	* Your code should look like this:

```
print("Hello World!")
```

* This doesn't look much like a story though. Try changing the text to make it say something longer and more interesting!
	* For longer bits of text, programmers usually use triple apostrophies. This makes sure that nothing can go wrong if your text runs over multiple lines.

Here's my example (I even added a pretty border around the outside!):

```python
print('''
		* -------------------------------------------------------*
		Most people think that the cat is an unintelligent animal,
		fond of ease, and caring little for anything but mice and
		milk. But a cat has really more character than most human
		beings, and gets a great deal more satisfaction out of
		life. Of all the animal kingdom, the cat has the most
		many-sided character.
		* -------------------------------------------------------*
''')

```

## Task 2: Remembering data
When we ask the user for things later, we need to remember what they said! Computers don't do this automatically, we need to tell them to remember things. For this, we will use something called a variable.

#### Step List:
* Make a variable with a text value, using ``word = "hotdog"``
	* A variable is a way of storing a value. In this case, we'll store a string value.
	* Using the equals sign **assigns** a value to the variable. This is done so that we can **refer** to it later.
	* You should read it as "word refers to hotdog". That's how we assign things.
	* A string is a series of characters, like a word, letter or sentence. We need speech marks around the string to tell the computer that it's a string.
* ``name = "Jack"``
	* This is how we give a variable a value.
	* In front of the equals, there is the variable name. This doesn't need speech marks.
		* Variable names must start with a letter, and can only include the alphabet, numbers and underscores.
	* The equals says that the left is the same as the value of the right. This way, everytime we say ``name`` in the rest of the program, it's the same as saying ``"Jack"``.
* Try making a variable called ``surname``, and give it your last name.
* Now try printing the variable.
	* Remember that we don't need speech marks!
	* See what it printed out!


#### Got lost? Here's the code.
```python
name = "Jack"
surname = "Homebrew"

print(surname)
```

What's the point in using variables? The clue is in the name. We need to use the name in a hundred different places in a long program, but if we want to change it, then we will have to go to one hundred different places to do so.

With a variable, **we just have to change the value in one place**, and then everywhere else the value changes. We can vary what the value is. We can also change the value of it half way through a program.

## Task 3: Ask the user
<!-- Break into paragraphs -->
To let the user customise the story, they need to be asked to give the parts we need. Let's ask them some questions, and remember what they say so we can use them later.

#### Step List:
* Make a new variable with a text value.
	* Same as before. For example: ``job = "plumber"``
* Change that variable's value (the part of the right), to be ``input()``.
	* It's very important to have the brackets touching the word input, otherwise the code won't work!
	* When the user answers in the box, they don't need to put speech marks around what they type. The computer does this automatically when you use ``input()``.
* Run this code.
	* The program should come up with a little input box.
* Change your code to print the variable.

Your code should look like:

```python
job = input()

print(job)
```
The user doesn't know what to input unless they read the code! Let's make the pop-up box ask the user a question.

* Put your question inside the brackets of ``input()``, but remember the speech marks!
	* We still need speech marks because we are using words, not variables in our question.
* We can print multiple things in one go by using a comma in the print function.
	* The comma can't be in speech marks! We are not using it as a comma, but as a separator.
* Try printing ``"Your job is"`` before the ``job`` variable is printed.

#### Got lost? Here's the code.
```python
job = input("What is your job?")

print("Your job is", job)
```

Inputs allow the user to interact with the program. We use variables with them, so that the user can change what the program does. If we didn't use variables, the user would have to go into the code and modify it to print their name.

Using a variable means that we only have to ask the user once, and the values are changed everywhere!

## Task 4: Putting the story together
Now we've learnt all the skills to make out automated story creator. We'll guide you through, step by step, for making your story.

#### Step List:
* Come up with a great story, and leave some spots where the user can change the values. Maybe plan this part out on paper!

Here's a not so interesting story that I wrote up quickly:

```
person1 and person1 met at place1.
person1 said speech1 to person2, person2 replied speech2.
Then they went to place2, and did activity1.

The day ended with activity2, and person1 and person2 final.

```
With this plan, I can see all the variables that I will need to use easily!

* Let's ask the user for each of your variables.
	* Add the question in the brackets so that the user knows what to enter!
* Now print each variable where it should be, with the story in between.
	* This should be using commas, like we just did!


#### Got lost? Here's the code.
```python
# We ask the user all of the details
person1 = input("What is person 1 called?")
person2 = input("What is person 2 called?")
place1 = input("Where did they meet?")

speech1 = input("What did person 1 say?")
speech2 = input("What did person 2 reply?")

place2 = input("Where did they go after that?")
activity1 = input("What did they do?")

activity2 = input("How did the day end?")
final = input("What happened at the end of the day?")


# Now we're outputting the story
print(person1, "and", person2, "met at", place1, ".")
print(person1, "said", speech1, "to", person2, ".", person2, "replied", speech2 ".")
print("Then they went to", place2, "and did", activity1 ".")
print("The day ended with", activity2, "and", person1, "and", person2, final ".")
```
##### # What?
Are you wondering why some lines have normal english in them, and start with a ``#``? These are called comments. Once we put a ``#`` on a line, everything after that line is ignored by the computer. We can write whatever we like here!

Comments are used to remind programmers what is going on in the code. It helps to keep things easy to read, and helps other programmers understand what the does if they are lost or confused.

Also note that blank lines are completely ignored by the interpreter (the computer that reads the code).

## Challenge Task
Let's make the questions a bit more personal. Try and figure out how we can ask the user "What did Steve say?", the user entered ``person1`` as ``"Steve"``.
