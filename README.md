Comp 221 Final Project: Connect 4 Minimax AI with Alpha-Beta Pruning
================================
Team Name: ARK

Team Members:

Andrew Taylor

Richard Tian
           
Kiet Tran

Briefing: We are implementing a simple AI algorithm to perform as an undefeatable rival to the player in a game of Connect 4.
The algorithm we use is called Minimax algorithm with Alpha-Beta pruning. We have explained and analyzed this algorithm in our final poster.

### Programming Explanation
We use comp124graphics package to help us implement the graphics for the connect 4 game.

The package for our program is named as org.macalester.edu.comp221.connectfour.

In side our package, we have created 6 classes as follows:

ConnectFourGame: the main game board for connect 4 game, it handles the user mouse events to make a move, and triggers the AI calculation.
It also controls the overall game flow, which is to check if there is a winner (4 in a line) and notifies the user about the game status, and then
it will reset the game for another round.

Token: represent a token (a circle) in the game, its color represent the owner of the token (player or AI)

TokenRow: represent a vertical row of tokens in the game, which in our cases have 6 tokens, and there are 7 TokenRows (columns)
in our game.

VirtualGameBoard: a virtual gameboard with a 2D array to represent the tokens and the board, for the AI calculation to
make assumptions on a certain column, and generate the utility score for the current virtual gameboard that enables the AI algorithm
to select the best move.

MinimaxAI: the class responsible for the AI calculation using Minimax with alpha beta pruning algorithm, we decide to set the search depth to be 8 instead of 4 with
since we have implemented alpha beta pruning to optimize the algorithm. We have specify max winning socre and min winning score so that the AI can make the 
most imminent decision if it knows that there is a winner in a virtual board. The main method that are called by the main game board is called "makeDecision" which 
triggers the AI calculation.

AIWorker: this class implements Runnable interface for us to run the AI in a separate thread, so that the main game thread will not freeze
while the AI algorithm is running. 



