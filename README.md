step one: run this command to install pynput:
    pip install pynput
step two: place your osrs screen to a size you can repeat and log in, placing your dude in a place you can repeate. 

step three: create a file named whatever you want and put these at the top:
  from pynput.mouse import Button, Controller
  import time
  import random

  mouse = Controller()

step four: code it out. Here are the commands I use and what they do.

mouse.position = (x,y)
This sets your mouse position using 2 points as pixels.
example mouse.position = (100, 100) 
this sets the mouse 100 pixels from the left and top of your screen.

mouse.click = (Button.left, 1)
This clicks your mouse. can click either left or right button. Second number is the number of clicks. usually leave it at 1 unless you wanna spam click something maybe.

time.sleep(1)
this sleeps your program for however many seconds you place in there. 

random.randint(1, 2)
this returns a random number that is between the two given numbers. 


EXAMPLE
Lets say I want a program that runs forever moving back and forth between two points and clicks them. First I will set an infinite While loop then work in it.

While True:
#create infinite loop

  mouse.position(100, 200)
#sets the mouse position to 100 pixels from left and 200 from top

  time.sleep(1)
#sleeps program to let runescape catch up

  mouse.click(Button.left, 1)
#clicks once on this position

  mouse.position(50, 200)
#sets the mouse position to the left 50 pixels

  time.sleep(1)
#again, waiting 1 second

  mouse.click(Button.right, 1)
#right clicks once on this position

#and the whole thing repeats. ezpz

