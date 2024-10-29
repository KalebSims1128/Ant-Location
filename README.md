# Drone Tracking System

This is a Python-based tracking system designed to calculate the location of drones moving within a bounded grid. The drones follow a fixed 45° movement direction and change course upon encountering grid boundaries, making it possible to predict their location after a given time period.

## Features

- **Grid-based Tracking**: The drone's movement occurs within an N x M grid, where N is the number of rows and M is the number of columns.
- **Boundary Detection**: Drones bounce off grid boundaries, reversing direction accordingly while maintaining a constant speed.
- **File or User Input Options**: Supports both file-based input and interactive user input for tracking multiple drones over a series of test cases.
- **Output to File**: Final coordinates after the specified hours (H) are saved in `output.txt`.

## Program Structure

### Files Used
- **Input File**: Accepts an input file (specified by the user) with initial positions and grid dimensions for each test case.
- **Output File**: Outputs final positions of the drones in `output.txt`.

### Functions

- **`ant_movement(N, M, i, j, H)`**:
  - Calculates the drone's position on an N x M grid after `H` hours.
  - `i, j` are the initial coordinates, and the drone starts moving towards the top-right at a 45° angle.
  - Changes direction when hitting any grid boundary.

- **`file_reader(user_input)`**:
  - Reads input either from a file or interactively from the user.
  - Runs the `ant_movement` function for each test case and stores results in `output.txt`.

- **`main()`**:
  - Handles the input type and calls `file_reader`.
