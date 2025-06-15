
import random

def play_game():
    number_to_guess = random.randint(1, 100)
    attempts = 0

    print("🎮 Welcome to 'Guess the Number'!")
    print("I'm thinking of a number between 1 and 100. Can you guess it?")

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < number_to_guess:
                print("🔻 Too low! Try again.\n")
            elif guess > number_to_guess:
                print("🔺 Too high! Try again.\n")
            else:
                print(f"🎉 Congratulations! You guessed the number {number_to_guess} in {attempts} tries!")
                break
        except ValueError:
            print("⚠️ Please enter a valid number.\n")
# Start the game
play_game()




