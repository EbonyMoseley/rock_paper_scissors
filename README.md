# rock_paper_scissors
This program simulates a game of rock-paper-scissors.

import random

def main():
    # user determines number of rounds of the game
    rounds = eval(input("Enter the number of rounds: "))
    # user's and comp's choices
    lst = ["rock","paper","scissors"]

    # initializes the score
    user_score = 0
    comp_score = 0

    # starts game of rock-paper-scissors for how many rounds user entered
    for i in range(rounds):
        print()
        print("Round:" , i)
        user_choice = input("  enter rock, paper, or scissors: ")
        # comp chooses a random option
        comp_choice = random.choice(lst)
        
        # conditionals for each possible choice of game results
        if user_choice == "rock" and comp_choice == "scissors":
            # adds 1 to user score for each choice that user wins
            user_score = user_score + 1
            print(" " , user_choice , "smashes" , comp_choice , ", user wins!")
            print("  current score: user" , user_score , ", computer" , comp_score)
            
        elif user_choice == "paper" and comp_choice == "rock":
            user_score = user_score + 1
            print(" " , user_choice , "covers" , comp_choice , ", user wins!")
            print("  current score: user" , user_score , ", computer" , comp_score)

        elif user_choice == "scissors" and comp_choice == "paper":
            user_score = user_score + 1
            print(" " , user_choice , "cuts" , comp_choice , ", user wins!")
            print("  current score: user" , user_score , ", computer" , comp_score)
            
        elif user_choice == "paper" and comp_choice == "scissors":
            # adds 1 to comp score for each choice that comp wins
            comp_score = comp_score + 1
            print(" " , comp_choice , "cuts" , user_choice , ", computer wins")
            print("  current score: user" , user_score , ", computer" , comp_score)
            
        elif user_choice == "rock" and comp_choice == "paper":
            comp_score = comp_score + 1
            print(" " , comp_choice , "covers" , user_choice , ", computer wins!")
            print("  current score: user" , user_score , ", computer" , comp_score)
            
        elif user_choice == "scissors" and comp_choice == "rock":
            comp_score = comp_score + 1
            print(" " , comp_choice , "smashes" , user_choice , ", computer wins!")
            print("  current score: user" , user_score , ", computer" , comp_score)

        else:
            # adds 0 to both user and comp score when choice is a tie
            user_score = user_score + 0
            comp_score = comp_score + 0
            print(" " , user_choice , "and" , comp_choice , "is a tie")
            print("  current score: user" , user_score , ", computer" , comp_score)

                           
        # adds space after each round             
        print()
        
# statements below generate the results        
    # prints final score
    # outside the for-loop
    print("The final score is: user" , user_score , ", computer" , comp_score)

    
    if user_score > comp_score:
        print("You win!")
        
    elif user_score < comp_score:
        print("Computer wins!")
        
    else:
        print("It's a tie!")


main()
