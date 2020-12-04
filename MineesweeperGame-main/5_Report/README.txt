1. Problem Statement:
The game consists of clearing all the squares of a two-dimensional arrangement that do not hide a mine. Some squares will have a random mine while others will not. The user is asked to position a cell in the two-dimensional arrangement, if user does not find a mine, user will continue the game until user wins, otherwise will finish the game and the user will lose.

2. Description:
Minesweeper is a single-player puzzle game available on several operating systems and GUIs. At the start of a game, the player receives an n × m rectangular grid of covered squares or cells. Each turn, the player may probe or uncover a square revealing either a mine or an integer. This integer represents the number of mines adjacent to that particular square. As such, the number on a cell ranges from 1 to 8 and 0 is represented by B here, since a cell can not have more than eight neighbours. The game ends when the player probes a cell containing a mine. The objective of the game is to uncover every square that does not contain a mine.
Playing Minesweeper involves a fair amount of logic. A clever player will use the numbered cells to deduce the location of mines. For assistance, most implementations of Minesweeper allow the player to mark or flag possible mine locations. However, this is simply for bookkeeping as the game does not validate any flagged squares. Higher difficulties of Minesweeper involve a greater degree of deductive reasoning as the mine density (number of mines over number of cells) increases. Oftentimes, mines can not be deterministically located, and so the player must resort to guessing. 
There are three difficulty levels for Minesweeper: beginner, intermediate, and expert. There is a custom input also in which user can decide the board size and number of mines. Beginner has a total of ten mines and the board size is 9 × 9. Intermediate has 40 mines and also varies in size 16 × 16. Finally, expert has 99 mines and is always 16 × 30. Typically in beginner, guessing is rarely necessary. The numbers on squares tend to stay in the ones and twos with the occasional three. As the difficulty increases, guessing becomes more common with expert configurations having numerous instances of guessing. Furthermore, higher numbered cells are more prevalent; however eights or sevens are still uncommon.

3. Requirements:
.	Software Requirements:
1.	MinGW Compiler
2.	Code::Blocks IDE v20.03
.	Operating System:
Preferably Windows OS
.	Language:
C language

4. Test Plan:
	Should write a program that takes input as follows,
	The input consists of an arbitrary number of fields.
	The first line of input contains an integer which stands for the level of the game i.e., beginner, intermediate, expert and custom input. 
	The second line of each field contains two integers n and m which stands for the number of rows and columns of the field respectively.
	Each safe square is represented by an “_” character (without the quotes) and each mine square is represented by an “*” character (also without the quotes). 
	The first field line where n = m = 0 represents the end of input and should not be processed.
	At the start of the game the grid is completely filled with hidden squares.
	When player clicks on an empty square that has no mine next to it, it recursively reveals all other adjacent empty cells, until it gets to one that is numbered.
	When player clicks on an square containing a mine, then all squares will be revealed. 
	Player only win when clears all non-mined cells.


	The goal of the game is to find all the mines within an M x N field. For the help, game shows a number in a square which tells how many mines there are adjacent to that square.  If a field with a mine is clicked the game is over. Each field that is opened shows a number that depicts how many mines are in the neighbourhood of the field. For instance, take the following 4x4 field with 2 mines which are represented by an “ * ” .
*  _  _  _
_  _  _  _
_ *  _  _
_  _  _  _ 
The same field including the hint numbers described above would look like this
* 1 0 0
2 2 1 0
1 * 1 0
1 1 1 0
Another example with 3 x 5 field with 2 mines are
* *  _  _  _
_  _  _  _ _
_ * _  _  _
The same field including the hint numbers described above would look like this
* * 1 0 0
3 3 2 0 0
1 * 1 0 0


5. Expected Results
	If a player completes the game by finding all the mines then display with a message called “Game Win” 
	If a player find the Mine in game then display with a message called “You lost” and all squares are revealed.
