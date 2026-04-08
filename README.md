# game2048forcs32
Game 2048 by Emily Bronckers, Bronte Brough and Rosa Kooijmans

#Possible plan made by chatgpt
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


