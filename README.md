# Rock-papre-scissor-

import random
comp=["rock","scissor","paper"]
b=comp[random.randint(0,2)]

name=input("ENTER YOUR NAME : ")
for i in range(5):
    print("\U0001F600",end="")
print("\nWELCOME ",name," TO THE ROCK/PAPER AND SCISSOR GAME AND YOU HAVE ONLY FIVE CHANCES :")
remain=5
us=0
cs=0

for i in range(5):
    user=input("CHOOSE ROCK, PAPER OR SCISSOR : ")
    print(b)
    if user=="rock" and b=="scissor":
        print("YOU WIN")
        us+=1
        cs-=1
    if user=="rock" and b=="paper":
        print("YOU LOOSE")
        us-=1
        cs+=1
    if user=="rock" and b=="rock":
        print("IT'S A TIE!!")
        
    if user=="paper" and b=="scissor":
        print("YOU LOOSE")
        us-=1
        cs+=1
    if user=="paper" and b=="rock":
        print("YOU WIN")
        us+=1
        cs-=1
    if user=="paper" and b=="paper":
        print("IT'S A TIE!!")      
        
    if user=="scissor" and b=="paper":
        print("YOU WIN")
        us+=1
        cs-=1
    if user=="scissor" and b=="rock":
        print("YOU LOOSE")
        cs+=1
        us-=1
    if user=="scissor" and b=="scissor":
        print("IT'S A TIE!!")
    
    remain=remain-1
    print("YOUR SCORE IS : ",us)
    print("YOU HAVE ONLY ",remain," CHANCES ")
print("YOUR FINAL SCORE IS ",us,"AND COMPUTER SCORE  IS ",cs)
    
if us>cs:
    print("YOU WIN THE GAME ")
    print("\U0001F917"*5,end="")
elif us<cs:
    print("YOU LOOSE THE GAME ")
    print("\U0001F62A"*5,end="")
else:
    print("IT'S A TIE")
    print("\U0001F637"*5,end="")
