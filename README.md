import random
import math
#############taking inputs
lower=int(input("enter your lower bound:- "))
upper=int(input("enter your upper bound:- ")) 
############generating random number between the lower and upper
x=random.randint(lower, upper)
print("\n\tyou've only " ,
      round(math.log(upper-lower + 1, 2)),
            "chances to guess the integer!\n")
##########intializing the number of guesses.
count = 0
      #for calculating of minimum number of guesses depend upon range
while count<math.log(upper-lower+1,2):
    count +=1

    ##########taking guessing number as input
    guess=int(input("guess a number:- "))

    ########condition testing
    if x==guess:
        print("congrats you did it in", count,"try")
        ##########ONCE GUESS, LOOP WILL bREAK
        break
    
    elif x > guess:
        print("have one more try, your guessed was too small")
    elif x< guess:
        print("have one more try, your guessed was too high")
    if count>=math.log(upper-lower+1,2):
        print("\n The number is %d" %x)
        print("\tBetter luck next time!")
        
