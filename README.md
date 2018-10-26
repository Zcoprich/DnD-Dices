# War
## What is War?
War is a project designed to create a simplistic, electronic version of the card game of a the same name. It is a C++ designed program; thus, it must be run through an integrated development environment (IDE) such as Dev-C++ (the IDE I used to run the program). It consists of two header files, two class files, and a main file called war which begins the entire program. 

War is a one player game where the user competes against the computer in a game of War. The computer-generated deck of fifty-two is randomized, an imitation of shuffling the deck, and separated so that both the player and the computer both have twenty-six cards. The deck is designed based on real playing cards so the available cards are the same. Neither the player nor the computer are allowed to look at the cards. Both the player and computer will display the top card from their given deck and whichever card holds the higher rank value wins that turn. If the two ranks match, both players will place down two cards. The first card is hidden from view while the second one is used to determine the winner. If the ranks match again the process is repeated. This continues until only one player has all fifty-two cards.

## War.cpp File
The war file is the core of the War project. The purpose of the war file is to connect the other four files with the content within itself in order to run the project. Many of the variables used as a base for the two class files are created in the war file. 

When the user begins the program, the war file prints out the instructions on how to play war. It will then have the computer ask the player whether he or she would like to have the cards dealt out to begin the game or would like to quit the program. The computer will prompt this each time they are about to deal a card. If the player decided to quit the program the program will end. 

If the player agrees to play the game it will deal out two decks of twenty-six from the fifty-two deck. The player and computer will display the topmost card of their deck, which will be printed on the screen in the order ‘rank/suit’. The ranks are the numbers 2 through 10 as well as the Jack, Queen, King, and Ace. The suits are Hearts, Diamonds, Clovers, and Spades. The computer will compare the rank of the two cards and determine a winner for that match. If the player wins, he or she gets to add both cards to their deck. If the computer wins, the computer adds both cards to its deck.

If the two cards are of the same rank, the player and computer go into a war (the namesake of the game). The player will be placed in a temporary loop where both the player and the computer places down two cards. The first card is hidden from view while the second card is used to determine the winner. The winner then receives all cards and the game returns to displaying one card at a time. If the second cards are of the same rank as well, the player and computer will repeat the process until one wins.

The program will win once the player or computer has all the cards or the player decides to quit the program.


## Card.h and Deck.h files
Unlike the other three files, the card header file and the deck header file consists of only the basics of a class file. They act as a basic outline for the card file and the deck file. The constructor and methods are originally defined here but are not fully developed. However, all methods and variables created in the header file must be implemented (though they do not have to be run in the program) in the appropriate class file. The other difference between the header file and its corresponding class file is that the header file has a ‘.h’ extension at the end of its name while the class file and main has a ‘.cpp’ extension added.

## Card.cpp
The card file is designed to create a card that will be added into a deck created by the deck file. Each card is created based on actual playing cards, so the ranks are the numbers 2 through 10 as well as the Jack, Queen, King, and Ace and the suits are Hearts, Diamonds, Clovers, and Spades. The class is designed to create only one pairing of rank and suit, so there will be no duplicates within the deck.

The card file also consist of the `get_rank()` method and a `get_suit()` method. Both methods are used to display the card’s value on the computer. However, only the `get_rank()` method is used to determine the winner of a turn. 

## Deck.cpp
The deck file’s purpose is to create the grid the initial fifty-two deck using the card file. It will then randomly separate the cards within the first deck to make two decks consisting of twenty-six cards. When the players attempt to draw a card, the computer uses the `draw _card()` method to implement the action. It also subtracts from the deck’s size. The `insert_card()` method allows the winner to add all won cards to his or her deck, increasing the deck’s size. The `get_size()` method is used to determine the player’s current number of cards.

## Project_3.dev
I have stated there are five important files that make up War. However, I have provided six files in the repository. Due to the design of C++, the main function cannot immediately connect all other files in order to run War. 

When creating a program that will consist of two or more class/header files, it is important to place them in a project file. Project_3.dev is an example of a project file. Its main purpose is to link all five files together so that the program can run. It does not contain any code that directly affects how the program itself is ran. It is also often created by the computer when placing all the files into a project.

If the project will not run but all files needed have been tested to compile smoothly, it is best to create a new project in a C++ IDE and transfer all files to the new project. The previous project file may not have properly been created, leading to a linking error in the program.
