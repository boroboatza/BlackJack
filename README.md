# BlackJack
A C++ implementation of a simple Blackjack game.

Here is a brief overview of what the code does:

The user is prompted to press 1 to start the game or 0 to exit.
If the user selects 1, the game starts, and the user is shown the game controls and their current credit balance (initialized to $1000).
The user can place a bet of $10, hit (draw a card), or stop (keep their current hand).
The dealer also draws cards and tries to get as close to 21 as possible without going over.
If the user's hand exceeds 21, they lose, and the dealer wins the bet. If the user's hand is less than or equal to 21, but the dealer's hand exceeds 21, the user wins the bet.
If both the user and dealer's hands are less than or equal to 21, the hand with the highest total wins the bet.
The game continues until the user decides to stop or runs out of credit.

However, the implementation has some issues and inefficiencies. Here are a few observations:

The implementation uses the conio.h header file, which is not a part of the standard C++ library. It's better to avoid using non-standard libraries to make the code more portable and avoid compatibility issues.
The implementation uses a lot of global variables, which can lead to naming conflicts and make the code harder to maintain. It's better to pass variables as arguments to functions whenever possible.
The implementation does not check for invalid user input. For example, if the user presses a key other than q, w, e, or r, the program does not handle it properly.
The implementation does not check for integer overflow when calculating the total value of the user's hand. If the user's hand contains many aces, the program may produce incorrect results.
The implementation does not provide an option to split pairs or double down, which are common features of Blackjack.
The implementation uses Sleep(1000), which is not the best way to pause the program for a second. It's better to use a timer or a loop to achieve a more accurate pause.
