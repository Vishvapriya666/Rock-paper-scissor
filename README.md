# Rock-paper-scissor
This program is designed to play rock, paper scissors, a classic children's game using python programming. 
import random, sys
print (" ****** Rock Paper Scissors ******")
# Trck win, loss and tie
win = 0
loss = 0
tie = 0

#Loop the main game.
while True:
    print(f"win: {win} nloss: {loss} nTie: {tie}")
    print("""Enter Your Move:
             r - Rock
             p - Paper
             s - Scissors
             q - quit""")
    UserMove = input("n Type one of the r, p s or q : ")

        
#Display what the computer choice: 
randomNumber = random.randint(1,3)

#Let the computer choose it's move.
if randomNumber == 1: 
    computerMove = 'r'
    print("Rock")
elif randomNumber == 2:
    computerMove = 'p'
    print("Paper")
elif randomNumber == 3:
    computerMove = 's'
    print("Scissors")
    
#Check win
if UserMove == computerMove:
    print("It is tie: !")
    tie += 1 
elif UserMove == 'r' and computerMove == 's':
    print("You win!")
    win += 1
elif UserMove == 'p' and computerMove == 'r':
    win += 1
    print("You win!")
elif UserMove == 's' and computerMove == 'p':
    win += 1
    print("You win!")
elif UserMove == "p" and computerMove == 's':
    loss += 1
    print("You lose!")
elif UserMove == "s" and computerMove == 'r':
    loss += 1
    print("You lose!")
