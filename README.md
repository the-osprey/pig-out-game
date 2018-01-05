# pig-out-game
Modified version of Pig Out game called Hog. Created for computer science sixty-one A at Berkeley!

Run the game by starting the GUI:
python3 hog_gui.py

Also, the game has some rudimentary AI that has a strategy. The winrate was about 60%. run it here:
python3 hog.py -r

Here are the rules, taken from the course website:

In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. 
On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for 
the turn is the sum of the dice outcomes.

To spice up the game, we will play with some special rules:

-Pig Out. If any of the dice outcomes is a 1, the current player's score for the turn is 1.

Example 1: The current player rolls 7 dice, 5 of which are 1's. They score 1 point for the turn.
Example 2: The current player rolls 4 dice, all of which are 3's. Since Pig Out did not occur, 
they score 12 points for the turn.

-Free Bacon. A player who chooses to roll zero dice scores one more than the largest digit in the opponent's total score.

Example 1: If the opponent has 42 points, the current player gains 1 + max(4, 2) = 5 points by rolling zero dice.
Example 2: If the opponent has 48 points, the current player gains 1 + max(4, 8) = 9 points by rolling zero dice.
Example 3: If the opponent has 7 points, the current player gains 1 + max(0, 7) = 8 points by rolling zero dice.

-Swine Swap. After points for the turn are added to the current player's score, if 
both scores are larger than 1 and either one of the scores is a positive integer multiple 
of the other, then the two scores are swapped.

Example 1: The current player has a total score of 37 and the opponent has 92. The current player rolls two dice that total 9. The opponent's score (92) is exactly twice the player's new total score (46). These scores are swapped! The current player now has 92 points and the opponent has 46. The turn ends.
Example 2: The current player has 91 and the opponent has 37. The current player rolls five dice that total 20. The current player has 111, which is 3 times 37, so the scores are swapped. The opponent ends the turn with 111 and wins the game.

