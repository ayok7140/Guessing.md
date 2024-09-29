# Guessing.md
# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start Game]) --> GenerateNum[Produce a Random Number]
    GenerateNum --> InputGuess[User Gives An Input]
    
    InputGuess --> CheckRange{Is Your Guess Within Range?}
    CheckRange -- No --> Invalid[Invalid Data; Try Again] --> InputGuess
    CheckRange -- Yes --> CheckGuess{Is My Guess Correct?}
    
    CheckGuess -- Yes --> Correct[Right, the final phase] --> End([End])
    CheckGuess -- No --> Feedback{Is it too high or too low?}
    
    Feedback -- Too High --> TooHigh[Way Too High! Try Again] --> InputGuess
    Feedback -- Too Low --> TooLow[Too Little! Try Again] --> InputGuess
