```mermaid
flowchart LR
    Start("Start Game")
    --> 1("Auto Generate Random Number 1-100(G#)")
    --> 2("Ask User To Guess G#")
    --> 3("Compare User Number (U#) to G#") --> 5.1 & 5.2 & 5.3 & 4
    4("If U# Has A Syntax Error, Display Syntax Error Message") --> 2
    5.1("If U# == G#, Display Winner Message") --> End
    5.2("If U# < G#, Display Higher Hint") --> 2
    5.3("If U# > G#, Display Lower Hint") --> 2
    End("End Game")
```

Node "**Start**" is just the start of the game.

**1** generates a random number between 1 and 100.

**2** asks the user to guess the generated number.

On **3**, the game compares the user's guess to its generated number.

**4** brings the user back to **2** if there is a syntax error in their guess.

If not, then **5.1** displays a winning message if the computer reads that the user's guess is correct.

If it is *less* than the generated number, **5.2** will bring the user back to **2** where they will have to guess again.

If it is *greater* than the generated number, **5.2** will bring the user back to **2** where they will have to guess again.

Once the correct guess is found, node "**End**" ends the game.
