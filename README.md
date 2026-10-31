#  # PIG
You against another player that needs to be with you. You choose when to roll the dice and when to hold.
## How to play

1. Click **roll** as many times as you want to get points.
2. If your dice rolls a 1 you lose all your turn points and its  the turn of the next player.
3. Press **hold** to save the points you won in the current round and pass your turn
4. Reach 100 points before your opponent or survive until your rival rolls 5 times 1 losing all of his lives.

## What I added
 
- Added lives and each time you roll a 1 you lose 1 live, ran out of lives and game over.And a message when you lose for loss of lives
- Also modified the text of the part that tells you the turn and what you rolled.
- Now the text in the hold button tells you how much points you will get if you hold
- Now if you roll two 6s in a row you lose your turn and turn total points and 1 live
Code added by gemini:   else if losesTurn(lastRoll: lastRoll, currentRoll: roll) {
 // Rolling two 6s in a row loses turn total and ends the turn.
            message = "Two 6s in a row! Player \(currentPlayer) loses \(turnTotal) points."
            turnTotal = 0
            lastRoll = 
            switchPlaye()
        }
- Also it says your last roll next to your turn total.
- If you try to click hold or roll when the game is over it will start a new game.
## How it works
Lives
- I added two variables for the lives of each player, they reset each time you click new game.
- Then I added two if, else if and two booleans that check if the lives of the player run out  in the function rollDie. One if, else if checks if a 1 was rolled and whose turn it is so it can subtract 1 live to that player
- There is an other else if that checks each time you roll the bools playerOneLost and playerTwoLost and if they are true (the lives of player lives equal to 0) the game is over.
- I added a new variable called holdShow (shows you hold will add) and it is an integer that resets to 0 each time you click new game and each time you switch player.
- I added an if, else so it checks what player is rolling the dice and the if, else was added in the two variables so it uploads the value each time you roll and swich player.
Two sixes in a row
-    Using the hint in the ideas part I created a new function that is bool so when its true it will be called back in rolldie and also added a var that embers your last roll
- In rolldie I called back losesTurn if lastRoll and currentRoll are 6 and it resets the turn total and the lastRoll substracts 1 live and switches the player.
- It says your last roll just by adding the text that says your last roll is and the variable lastRoll with a / and ().
restarts the game when its over and you click hold or roll 
- added an if in the functions roll and hold that checks if the boolean gameIsover is true each time you click or roll and if it is it restarts the game.
-

## Testing
| Test | Chosen Input | Should happen | Did happen |
| --- | --- | --- | --- |
| roll is just 1 or 6 | click 2 times roll and then hold 2 times | players should probably get no points or maybe 12 |  player 1 got 12 points player 2 got 0     points |
| lives is equal to 1 | play until someone rolls a 1 | the player that did not roll the 1 should win| the player that rolled 1 lost the other one won |
| winning score is 50 | Play until a player reaches 50 points or more | the player that reaches 50 points should win | the player that reached 50 won |
|roll is just 5 and 6|click 10 times roll  | the player should get 10 , 11 or no points | the player got no points |  
 | Two 6s in row |Roll fixed at 6; player 1 clicks roll twice  |  Player loses 6 points his turn and one live |  the player lost his turn points and one live |
|Two rolls the same, not 6  |Roll fixed at 5: Player  clicks roll twice and      then hold |  Player 1 should get 10 points | Player 1 got 10 points |
| What hold shows | Roll fixed at 4: player 1 clicks roll three times and then holds |   player 1 should get 12 points | player 1 gets 12 points | 
|  One live left (edge)| Lives start at 2 roll fixed at 1 and player one   cliks roll |  Player one should lose one live | player 1 lost one live |
| Last live(edge) | Lives start at 1 roll fixed at 1 and player one   cliks roll |  Player 1 should lose | player 1 lost |
|  after the game is over|As the last row, then click roll 1 more time  |  nothing should happen | thegame kept going with negative lives |
| When a player runs out of lives |  play until a player runs out of lives and then click roll or hold. |  it should restart the game |  the game restarts |
|  When a player wins |  play until a player wins and then click roll or hold.|  it should restart the game|   the game restarts|



 


## Credits
 
- The starting game was written by Mr. Gordon.
- The rest was written by Diego de Oteyza
- Gemini helped with the programm

            
