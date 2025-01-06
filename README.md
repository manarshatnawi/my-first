step 1 : 
Name student1 : manar shatnawi , student number : 202210366
Name sudent2 : yara khanfar , student number : 202220702
Team code : H                                                                                                                           

step 2 : 
The dataset you have described contains several columns related to a guessing game where players try to break a secret code. Here's an explanation of each column:

secret_code: This column represents the secret code that the player needs to guess. The code is typically hidden from the player, and their objective is to correctly guess it through a series of attempts.

guess: This column contains the player's guess for the secret code. It reflects the code they attempted to match with the secret one.

guesses_left: This column shows the number of guesses the player has left after making a specific guess. It indicates how many attempts the player can still make before running out of guesses.

success: This column indicates whether the player successfully guessed the secret code ("Yes" or "No"). If the player correctly guesses the code, this will be marked as "Yes," otherwise it will be marked as "No."

player_name: This column includes the name of the player who is participating in the game.



step 3 : 


The provided code implements a simple console-based game called "Secret Code Breaker." The objective of the game is for the player to guess a randomly generated 4-digit code, with feedback provided after each guess. Below is a detailed explanation of the code:

### Imports
- pandas: Used for handling high scores, reading from and writing to CSV files.
- random: Used to generate random numbers for the secret code.
- matplotlib.pyplot: Used for plotting the player's progress in terms of correct guesses.

### Class Definition:
SecretCodeBreaker

This class encapsulates the game's functionality.

#### Initialization Method:
init

- Initializes the game state:
-
self.code
: Stores the secret code (initially empty).
-
self.attempts_left
: Number of attempts the player has to guess the code (set to 3).
-
self.player_name
: Stores the player's name (initially empty).
-
self.correct_digits_progress
: List to track the number of correct digits in each attempt.

#### Method:
generate_code

- Generates a random 4-digit code where each digit is between 1 and 9. This code is stored in
self.code
.

#### Static Method:
validate_guess

- Validates the player's guess:
- Ensures the guess is exactly 4 digits long.
- Checks that each digit is a number between 1 and 9.

#### Method:
get_feedback

- Compares the player's guess with the secret code:
-
correct_position
: Counts how many digits are in the correct position.
-
correct_digit
: Counts how many digits are correct but in the wrong position.
- Returns both counts.

#### Static Method:
read_high_scores

- Attempts to read high scores from a CSV file (
high_scores.csv
):
- If the file exists, it loads the scores into a DataFrame.
- If the file does not exist, it initializes an empty DataFrame for high scores.
- Handles any exceptions that may occur during file reading.

#### Static Method:
save_high_scores

- Saves the high scores DataFrame to a CSV file:
- If successful, it confirms the save operation.
- Handles any exceptions that may occur during file writing.

#### Method:
plot_progress

- Plots the player's progress in terms of correct digits guessed over attempts:
- If there is no progress data, it informs the user.
- Uses matplotlib to create a line plot.

#### Method:
play_game

- Main game loop:
- Calls
generate_code
to create a new secret code.
- Prompts the player for their name.
- Allows the player to make guesses until they run out of attempts or guess the code correctly.
- Validates each guess and provides feedback.
- Tracks the number of correct digits and saves high scores if the player wins.

### Main Program Loop:
main

- Initializes the game and presents a menu to the player:
- Option to play the game.
- Option to view high scores.
- Option to exit the game.
- Based on the player's choice, it either starts a new game, displays high scores, or exits.

### Entry Point
- The last line checks if the script is being run directly and calls the
main
function to start the game.

### Summary
This code provides a complete implementation of a guessing game where players attempt to guess a secret code. It includes features for validating input, providing feedback, tracking progress, and saving high scores. The use of classes and methods encapsulates the game's logic, making it modular and easy to understand.
