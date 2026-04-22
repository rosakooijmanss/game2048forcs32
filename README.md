# game2048forcs32
Game 2048 by Emily Bronckers, Bronte Brough and Rosa Kooijmans

Description
Our final project computes the famous game 2048. You win the game whenever the tile 2048 is created. However, when there are no white spaces left on the board, you lost the game. The player has the ability to move tiles left, right, up, or down. Whenever two tiles with the same numbers are merged, the added result is put in only one tile. With every move, the game randomly adds either a 2 or 4 (especially 2's) in any of the white spaces. As the game continues, the board therefore becomes fuller with higher numbers, while it takes more tiles to create the next number. That makes it hard to get higher up to 2048 without having a full board in the meantime.

Instructions to run it
The player has 4 options every time: arrow left, right, up, or down. It will keep putting in any of these inputs untill the game is either lost or won. 

Special set up steps


Internet and aI 
In detail, which pieces

Add to your README.md a description of what your project does and instructions for running your code. If this requires any special set-up steps (e.g., using a local IDE, uploading certain files, installing packages, obtaining a personal API key, etc.), be sure to explain those steps.
Cite any external contributors (so far) in your README.md. If pieces of your code came from the Internet, such as from a tutorial, give credit with a link to that source. If you used generative AI tools, please describe in detail how you used those tools, and which code pieces, if any, it wrote for you.
Check your work into your GitHub repository (instructions). Make sure your mentor has access to your repository.



write 4x4 board like a list of lists:
board = [
    [2, 0, 2, 4],
    [0, 4, 4, 0],
    [2, 2, 0, 0],
    [0, 0, 0, 2]
    ]
write what happens when player does a move (either left, right, up or down)
input: move and output: new board after that move
possible functions:
print_board(board)
compress(row) to move nonzero numbers left trick is to fully implement left and define other directions by rotating/reversing the board
steps:
1. remove zeros
2. merge equal neighbors once
3. remove gaps again
4. pad with zeros on the right
merge(row) to merge equal numbers
move_left(board)
move_right(board)
move_up(board)
move_down(board)
add_new_tile(board): place a 2 or 4 in a random empty square
game_over(board): no more valid moves
won(board): tile 2048 exists

For first video:
initial board representation
implemented print_board


