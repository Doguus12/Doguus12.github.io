# Guessing Game Flowchart

```mermaid
flowchart TD
    A([Start]) --> B[Generate random number]
    B --> C[Get user guess]
    C --> D{Is input valid?}
    D -->|No| E[Display error message]
    E --> C
    D -->|Yes| F{Is guess correct?}
    F -->|Yes| G[Display win message]
    F -->|No| H{Is guess too high?}
    H -->|Yes| I[Display 'too high' message]
    H -->|No| J[Display 'too low' message]
    I --> K{Play again?}
    J --> K
    G --> K
    K -->|Yes| B
    K -->|No| L([End])
## Process Description

1. Start: The program begins.
2. Generate random number: The computer selects a random number within a specified range.
3. Get user guess: The program prompts the user to input their guess.
4. Is input valid?: The program checks if the user's input is a valid number within the game's range.
   - If not valid, display an error message and ask for another guess.
   - If valid, proceed to check if the guess is correct.
5. Is guess correct?: Compare the user's guess with the generated number.
   - If correct, display a win message.
   - If incorrect, check if the guess is too high or too low.
6. Display feedback: Tell the user if their guess was too high or too low.
7. Play again?: Ask the user if they want to play another round.
   - If yes, generate a new random number and start over.
   - If no, end the program.
8. End: The program terminates.