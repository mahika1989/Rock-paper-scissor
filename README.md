# Rock-paper-scissor
import random
c=0
d=0
while True:
    user_action = input("Enter a choice (rock, paper, scissors): ")
    possible_actions = ["rock", "paper", "scissors"]
    computer_action = random.choice(possible_actions)
    print("User:",user_action)
    print("CPU:",computer_action)


    if user_action == computer_action:
        print(f"Both players selected {user_action}. It's a tie!")
    elif user_action == "rock":
        if computer_action == "scissors":
            print("You win! Rock smashes scissors!")
            c+=1
        else:
            print("You lose, Paper covers rock!")
            d+=1
    elif user_action == "paper":
        if computer_action == "rock":
            print("You win! Paper covers rock!")
            c+=1
        else:
            print("You lose, Scissors cuts paper!")
            d+=1
    elif user_action == "scissors":
        if computer_action == "paper":
            print("You win, Scissors cuts paper!")
            c+=1
        else:
            print("You lose, Rock smashes scissors!")
            d+=1

    play_again = input("Play again? (y/n): ")
    if play_again.lower() != "y":
        break
if c==d:
    print("It's a tie")
    print("CPU:",d)
    print("User:",c)
elif c>d:
    print("You win")
    print("CPU:",d)
    print("User:",c)
elif c<d:
    print("You lose")
    print("CPU:",d)
    print("User:",c)
