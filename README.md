# towers-of-hanoi

Initialization:

    The program imports the Stack class from the stack module and initializes three stacks (left_stack, middle_stack, right_stack) representing the three pegs in the Towers of Hanoi game.
    It prompts the user to input the number of disks to play with either through command-line arguments (sys.argv[1]) or user input if no arguments are provided.

Input Validation:

    It ensures that the number of disks (num_disks) is at least 3 to proceed with the game.

Game Setup:

    The disks are initially placed on the left_stack in descending order of size.

Optimal Moves Calculation:

    It calculates the optimal number of moves (num_optimal_moves) required to solve the game using the formula 2num_disks−12num_disks−1.

User Input Function (get_input):

    Defines a function get_input() to prompt the user to select a stack from which to move disks (from_stack) and a stack to which to move disks (to_stack).
    It validates the user's input and returns the selected stack object.

Game Execution:

    Enters a loop where the game continues until all disks are moved to the right_stack (peg).
    During each iteration:
        It displays the current state of the stacks.
        It repeatedly prompts the user to choose a stack to move from and a stack to move to.
        It validates the move:
            Ensures the stack to move from (from_stack) is not empty.
            Ensures the move is valid (e.g., moving smaller disks on top of larger disks is not allowed).
        If a valid move is made, it updates the stacks accordingly and increments num_user_moves.

Game Completion:

    Once all disks are moved to the right_stack, it prints the number of moves the user took (num_user_moves) compared to the optimal number of moves (num_optimal_moves).
