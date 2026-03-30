import random

# Function to get computer choice
def get_computer_choice():
    return random.choice(["rock", "paper", "scissors"])


# Function to decide winner
def decide_winner(user, computer):
    if user == computer:
        return "tie"
    elif (user == "rock" and computer == "scissors") or \
         (user == "scissors" and computer == "paper") or \
         (user == "paper" and computer == "rock"):
        return "user"
    else:
        return "computer"


# Main game
def play_game():
    user_score = 0
    computer_score = 0

    print("====== ROCK PAPER SCISSORS GAME ======")
    print("Type 'rock', 'paper', or 'scissors' to play.\n")

    while True:
        user_choice = input("Your choice: ").lower()

        if user_choice not in ["rock", "paper", "scissors"]:
            print("Invalid choice! Try again.\n")
            continue

        computer_choice = get_computer_choice()

        print(f"\nYou chose: {user_choice}")
        print(f"Computer chose: {computer_choice}")

        result = decide_winner(user_choice, computer_choice)

        if result == "tie":
            print("It's a tie!")
        elif result == "user":
            print("You win! 🎉")
            user_score += 1
        else:
            print("Computer wins! 🤖")
            computer_score += 1

        print(f"\nScore -> You: {user_score} | Computer: {computer_score}")

        # Play again option
        again = input("\nPlay again? (y/n): ").lower()
        if again != 'y':
            print("\nThanks for playing! 👋")
            break

        print("\n---------------------------\n")


# Run the game
if __name__ == "__main__":
    play_game()
