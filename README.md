Name student1 : manar shatnawi , student number : 202210366
Name sudent2 : yara khanfar , student number : 202220702
Team code : H 
The project utilizes a CSV file named
high_scores.csv
to store and retrieve high scores of players. This dataset contains the following columns:

- Player: The name of the player who participated in the game.
- Remaining Guesses: The number of attempts the player had left when they successfully cracked the code.

If the file does not exist, the program initializes an empty DataFrame with these columns to start a new high score list.

### Function and Class Descriptions

The project consists of several functions, each serving a specific purpose. Below is a detailed description of each function, including methods, loops, and conditional statements used within them.

1.
generate_code()

- Purpose: Generates a random 4-digit code where each digit is between 1 and 9.
- Method:
- Uses a list comprehension to create a list of 4 random integers.
- Loop:
- A
for
loop iterates 4 times to generate each digit.

2.
validate_guess(guess)

- Purpose: Validates the player's guess to ensure it meets the criteria.
- Method:
- Returns
True
if the guess is exactly 4 digits long and each digit is between 1 and 9.
- Conditional Statements:
- Uses
all()
to check if all conditions for each digit are met.

3.
get_feedback(code, guess)

- Purpose: Provides feedback on the player's guess compared to the generated code.
- Method:
- Calculates the number of digits in the correct position and the number of correct digits in the wrong position.
- Loops:
- A
for
loop iterates over the indices of the code to count correct positions.
- Conditional Statements:
- Uses
set()
to find unique digits in the guess for counting correct digits.

4.
read_high_scores()

- Purpose: Reads high scores from the CSV file.
- Method:
- Attempts to load the high scores into a DataFrame.
- Conditional Statements:
- Uses
try-except
to handle file reading errors, returning an empty DataFrame if the file is not found.

5.
save_high_scores(df)

- Purpose: Saves the high scores DataFrame to the CSV file.
- Method:
- Writes the DataFrame to a CSV file.
- Conditional Statements:
- Uses
try-except
to handle potential errors during file writing.

6.
plot_progress(guesses_data)

- Purpose: Plots the progress of correct digits over each guess.
- Method:
- Uses Matplotlib to create a line plot.
- Conditional Statements:
- Checks if there is data to plot; if not, it prints a message.

7.
play_game()

- Purpose: Main function to run the game.
- Method:
- Generates a random code and manages the game loop.
- Loops:
- A
while
loop continues until the player runs out of attempts or cracks the code.
- Conditional Statements:
- Checks for valid guesses and provides feedback; also checks if the player has won.

8.
show_high_scores()

- Purpose: Displays the high scores.
- Method:
- Reads high scores and prints them if available.
- Conditional Statements:
- Checks if the DataFrame is empty before printing.

9.
main()

- Purpose: Main program loop to interact with the user.
- Method:
- Provides options to play the game, show high scores, or exit.
- Loops:
- A
while
loop continues until the user chooses to exit.
- Conditional Statements:
- Checks user input to determine the action to take.

### Summary of Control Structures

- Loops: Primarily
for
loops are used for generating random codes and counting correct positions, while
while
loops manage the game flow and user interaction.
- Conditional Statements:
if
statements are extensively used to validate inputs, check game conditions, and handle exceptions.

This structured approach ensures that the game operates smoothly while providing a user-friendly experience.
the output : Welcome to the Secret Code Breaker Game!

Choose an option:
1. Play Game
2. Show High Scores
3. Exit
>  1
Enter your name:  yara
Hello yara! Let's start the game.

You have 3 attempts left.
Enter your guess (4 digits between 1 and 9):  4251
Feedback: 0 correct position(s), 1 correct digit(s) in wrong position(s)

You have 2 attempts left.
Enter your guess (4 digits between 1 and 9):  7845
Feedback: 0 correct position(s), 2 correct digit(s) in wrong position(s)

You have 1 attempts left.
Enter your guess (4 digits between 1 and 9):  9874
Feedback: 0 correct position(s), 2 correct digit(s) in wrong position(s)

Sorry! You've run out of attempts. The correct code was: 6718
