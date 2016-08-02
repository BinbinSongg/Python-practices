# Python-practices
Some simple exercises by using Python

1.Function exercises--project 
Objective:
In this project, we'll build a program that rolls a pair of dice and asks the user to guess a number. Based on the user's guess, the program should determine a winner. If the user's guess is greater than the total value of the dice roll, they win! Otherwise, the computer wins.

The program should do the following:

Randomly roll a pair of dice
Add the values of the roll
Ask the user to guess a number
Compare the user's guess to the total value
Decide a winner (the user or the program)
Inform the user who the winner is

#codes below 
'''A guess game by rolling dice'''
from random import randint 
from time import sleep 

#Functions-for user and computer 
def get_user_guess():
    user_guess=int(raw_input('Your guess: '))
    return user_guess

def roll_dice(number_of_sides):
    first_roll=randint(1,number_of_sides)
    second_roll=randint(1,number_of_sides)
    max_val=number_of_sides*2
    print 'The maximum possible value is: '+ str(max_val)
  
    sleep(1)

    user_guess=get_user_guess()

    #decide who is the winner 
    if user_guess>max_val:
      print 'The guess is invalid!'
      return
    else:
      print 'Rolling...'
      sleep(2)
      print 'The first rolling number is: %d' % first_roll
      sleep(1)
      print 'The second rolling number is: %d' % second_roll
      sleep(1)
      total_roll=first_roll+second_roll
      print'The total roll is: %d' % total_roll
      print'Result...'
      sleep(1)
      if user_guess>total_roll:
        print'You won!'
      else:
        print'You lost!'
 
roll_dice(6)
    
  
  
  
  
