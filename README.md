# game2048forcs32
Game 2048 by Emily Bronckers, Bronte Brough and Rosa Kooijmans



Description

Our final project computes the famous game 2048. You win the game whenever the tile 2048 is created. However, when there are no white spaces left on the board, you lost the game. The player has the ability to move tiles left, right, up, or down. Whenever two tiles with the same numbers are merged, the added result is put in only one tile. With every move, the game randomly adds either a 2 or 4 (especially 2's) in any of the white spaces. As the game continues, the board therefore becomes fuller with higher numbers, while it takes more tiles to create the next number. That makes it hard to get higher up to 2048 without having a full board in the meantime.



Instructions to run it

The player has 4 options every time: arrow left, right, up, or down. It will keep putting in any of these inputs untill the game is either lost or won. 



Internet and AI

We could come up with the idea to implement what would happen whenever the player would press the left arrow. A slide to the left would happen and with the help of our other functions, that would merge all of the same tiles and create a new board. However, it would become very long if we had to write this for all of the other three moves. We thought there would be a possibility of doing this smarter, so we asked ClaudeAI. It came up with the idea to still use the left slide option, but turn the board on every move. This would need a lot less code, so we used this idea. 

In step 1 of main sliding logic, we changed changed it in Claude AI from a for loop to a list to make our script shorter.

The next step in implementing what happens when one of the arrows is pressed, is turning the board. We knew how to shift it from left to right, using .... However, we did not know how to transpose the board, so we asked the internet how to transpose a 2D list. It gave us the idea to unpack the operator, zip the board, and then pair it. Below is the provided code.
[list(row) for row in zip(*board)] 

After we created all of the functions we wanted to create, we wanted to make sure they worked before implementing them in the right order. This could save a lot of time debugging when implementing the functions, as that would be very hard when the problem would lie in the function itself. Therefore, we asked AI to provide tests to check our functions. We fully copied these tests in our fp status and it helped us to debug our functions and eventually prove they worked. These we could then also show off in the status update.  

At first, we did not realise that there is a possibility that you did not lose, even when the board is full. We implemented only that condition. However, when there are two tiles with the same number next to eachother, you can still do a move without losing. We realised this when we used the tests. Then we asked ClaudeAI to help us implement that second condition, which is checking whether every cell had a mergeable neighbor. AI helped to find out we had to loop through all the tiles and only check for a mergeable neighbor to the right or below it. 




