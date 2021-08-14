# turtle_race
#importing turtle and random
from turtle import Turtle, Screen, width
import random

# is game start
is_race_on = False

# creating objects
turtle = Turtle()
screen = Screen()

# specifying screen size
screen.setup(width=700, height=600)

# make bet
make_bet = screen.textinput(title="Make Your Bet", prompt="Which turtle win the race? Enter a color(red, yellow, orange, green, blue, purple),: ",)

# turtle colors
colors = ["black", "blue", "red", "green", "white", "purple", ]

# turtle y-axis position for add gap with each other
position = [-70, -40, -10, 20, 50, 80]

# empty list for all turtle
all_turtle = []

for turtle_index in range(0, 6):
    # turtle shape
    turtle = Turtle(shape="turtle")
    # stop pen writing
    turtle.penup()
    # add colors to turtle
    turtle.color(colors[turtle_index])
    # start from left edge of screen
    turtle.goto(x=-330, y=position[turtle_index])
    # add all turtle on the list
    all_turtle.append(turtle)

# checking make bet
if make_bet:
    is_race_on = True

# Start the game
while is_race_on:
