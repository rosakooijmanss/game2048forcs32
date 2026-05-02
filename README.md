# game2048forcs32
Game 2048 by Emily Bronckers, Bronte Brough and Rosa Kooijmans



This project is our own implementation of the classic game 2048, built completely from scratch in Python.

The goal is simple:
- Combine tiles
- Reach 2048
- Don't fill up the board before you get there

Every move shifts all tiles in one direction, merges equal numbers, and then randomly spawns a new tile (usually a 2 and sometimes a 4).


HOW THE GAME WORKS
- You play on a 4x4 grid
- Each move:
  - Slides all tiles in that direction
  - Merges tiles with the same value
- After every move:
  - A new tile (2 or 4) appears in a random empty cell
- You win when you reach 2048
- You lose when
  - The board is full and
  - No more merges are possible


HOW TO PLAY 
Run the program and use your keyboard:
- A = move left
- D = move right
- W = move up
- S = move down

The game continues until you either:
- Win (reach 2048)
- Lose (no moves left)



Internet and AI

We could come up with the idea to implement what would happen whenever the player would press the left arrow. A slide to the left would happen and with the help of our other functions, that would merge all of the same tiles and create a new board. However, it would become very long if we had to write this for all of the other three moves. We thought there would be a possibility of doing this smarter, so we asked ClaudeAI. It came up with the idea to still use the left slide option, but turn the board on every move. This would need a lot less code, so we used this idea. 

In step 1 of main sliding logic, we changed changed it in Claude AI from a for loop to a list to make our script shorter.

The next step in implementing what happens when one of the arrows is pressed, is turning the board. We knew how to shift it from left to right, using .... However, we did not know how to transpose the board, so we asked the internet how to transpose a 2D list. It gave us the idea to unpack the operator, zip the board, and then pair it. Below is the provided code.
[list(row) for row in zip(*board)] 

After we created all of the functions we wanted to create, we wanted to make sure they worked before implementing them in the right order. This could save a lot of time debugging when implementing the functions, as that would be very hard when the problem would lie in the function itself. Therefore, we asked AI to provide tests to check our functions. We fully copied these tests in our fp status and it helped us to debug our functions and eventually prove they worked. These we could then also show off in the status update.  

At first, we did not realise that there is a possibility that you did not lose, even when the board is full. We implemented only that condition. However, when there are two tiles with the same number next to eachother, you can still do a move without losing. We realised this when we used the tests. Then we asked ClaudeAI to help us implement that second condition, which is checking whether every cell had a mergeable neighbor. AI helped to find out we had to loop through all the tiles and only check for a mergeable neighbor to the right or below it. 


DISPLAY 
refined and enhanced




