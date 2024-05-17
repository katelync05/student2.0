## Final Project Plan

- Project Plan: Algorithms and Sudoku 

We plan to make a sudoku algorithm where the computer will generate and solve the puzzle with possibly a twist to make the game more interactive/visually appealing

- Set up 
    - Create tables for storing Sudoku puzzles, user data, and game states using SQLAlchemy.
    - Write scripts to create and initialize the database schema
- Backend 
    - Use a backtracking algorithm to generate valid Sudoku puzzles.
    - Store generated puzzles in the database.
    - Implement the backtracking algorithm for solving Sudoku puzzles.
- Allow users to interact with the Sudoku grid, input numbers, and submit puzzles for solving
- Algorithms
     - generate a list of the possible values (1-9) for each cell
     - filter out the values that are already present in the same row, column, or 3x3 subgrid
- Sorting / Searching with SQLAchemy
- Analyze and document the time and space complexity of the Sudoku solving algorithm.
- 2D iteration to validate and manipulate grid

Partner: Tanvi P.