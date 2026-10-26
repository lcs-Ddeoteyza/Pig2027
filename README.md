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
- Now the text in the hold button tells you how much points you will get if youh hold

## How it works
Lives
- I added two variables for the lives of each player, they reset each time you click new game.
- Then I added two if, else if and two booleans that check if the lives of the player run out  in the function rollDie. One if, else if checks if a 1 was rolled and whose turn it is so it can subtract 1 live to that player
- The other if, else if is constantly checking if the booleans are true or false so when someone loses it sends a win message.
Hold
- I added a new variable called holdShow (shows you hold will add) and it is an integer that resets to 0 each time you click new game and each time you switch player.
- I added an if, else so it checks what player is rolling the dice and the if, else was added in the two variables so it uploads the value each time you roll and swich player.

## Credits
 
- The starting game was written by Mr. Gordon.
- The rest was written by Diego de Oteyza
