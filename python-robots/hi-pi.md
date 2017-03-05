---
title: Hi, Pi
---

# Hi, Pi!
### Teacher's lesson plan
This is a lesson guide, intended for teachers to use when introducing the Raspberry Pi to students.

We'll be introducing them to the **command line**, with a few basic commands to help them navigate it (but we won't be dwelling on this); more importantly, we will be introducing them to the **graphical user interface (GUI)**, which is where we expect that they will spend most of their time developing code and hacking bits together. 

## Task 0: Don't break anything!
As soon as everyone has their Raspberry Pis, they'll be sure to be inspecting them, and poking about. But remember, the board itself has exposed electronics! If that doesn't ring alarm bells (with kids involved), then think of **static electricity!** 

If a potential difference exists between the students and the Pi, then touching some components can cause tiny sparks. These may not be fire hazards or at all harmful for the students, but can damage the components so that they have a reduced lifetime (meaning you'll have to throw them away *a lot* sooner than you'd hope). 

**Basically, just warn them not to touch it** – don't bother with the technicalities, and buy a case instead. A simple warning will do!

## Task 1: The Hardware
After the prodding around is done, we can briefly explain what as the stuff poking out of the board really is (that main parts anyway). 

**USB Ports** – these are the big blocks (2 by 2 if you're using the A+, B+, 2 or 3, and 1 by 2 if you're using the B or A), these let us plug things like keyboards and mice and printers and general things in. Get everyone to plug in a keyboard and mouse (and wifi dongle if you need to). 

**HDMI Port** – just one wide port on the side, lets us connect the device to a screen so that we can see what's going on. It stands for "high definition multimedia interface". Plug these into the screen (be careful not to have the power plugged in too, in case of dodgey cables). (Note: if you're working in a school, you've probably got an HDMI to something-else cable, so make sure that students know which ones go where [they will]). Connect up the screen!

**Ethernet Port** – a wired internet connection. You probably won't use these, thanks to the proxies that all schools have. It's faster than wifi usually, and is built in (unlike wifi dongles, which are plugged in, unless you're using the 3). 

**GPIO Pins** – these are the general purpose, input, output pins which let us interface from our Pi, out to the real world. We'll be using these a lot, and this is where you're most likely to damage your Pi by touching all of the pins at the same time (3V and 5V pins are live when the Pi is powered). 

**Slots** – there are multiple ribbon band connector slots on the surface of the Pi that you might not notice, for camera and the likes. 

**SD Card Reader** – at the bottom of the Pi, an SD card sits which runs the whole system. Taking this out whilst the system is still running will cause the whole system to crash, potentially leaving you with a corrupt SD card, which needs re-imaging. Everyone should know not to play with this when the Pi is on. 

**Power** – a micro USB connection gives the Raspberry Pi its life. That means we can use a phone charger (providing it has the right voltage rating). Connect up the Pi and watch the rainbow colours and green text on the screen!

## Task 2: The matrix
At this point, lots of the kids think that they are hackers. Hackers aren't all evil, but these kids definitely aren't them. We'll get everyone used to the Pi (which *hopefully* you've set up once, and connected to the internet, and then flashed to all of the SD cards to save time). 

Please don't leave them to set up the raspi-config screen!

### Login
Username: pi
Password: raspberry

No spaces! This is **always** the default password! Don't bother changing it either.

### ls
We've made it the command line interface, logged in and now what? It's not as neat as a GUI, so we have to manually look around. Start with listing all of the files in the directory (folder). 

```bash
ls
```

Now we can see the files! Okay that was fine, but nows lets move ourselves into a folder. 

### cd 
Change directory using cd, and then the folder name. Try documents.

```bash
cd Documents
```

Changing back to the folder before is as simple as `cd ..`, which goes to the parent folder.

### nano 
How do we write our code? Most easily, and usually we write in a text file. In the terminal, the easiest text editor is `nano`

Open a blank file with:

```bash
nano
```

To open an existing file, e.g. `myfile.txt`:

```bash
nano myfile.txt
```

So save the file and exit, press control and x, and then enter to save the existing file, or enter a filename and then save. 

### python3 
Running Python code on the command line is simple, using:

```bash
python3 myProgram.py
```

Remember that Python files should end with `.py` (and that we're using python3, for python 2.7, take out the 3). 

We can also write code straight into the interpreter, by just typing `python3`, but usually we don't want to do this. 

### pip3 etc.
If you think that your class are apted enough to know about packages and libraries then talk about pip and pip3, but we think this is too much for our year 7s!

### startx
This is all very slow for the kids, so lets launch the GUI (they'll be relieved), by typing:

```bash
startx
```

Finally!

## Task 3: IDLE3 and other apps

## Task 4: Shutting down properly

