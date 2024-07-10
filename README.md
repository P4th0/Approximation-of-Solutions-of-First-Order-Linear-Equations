# Approximation of Solutions for First Order Linear Differential Equations

## Project Description
This Python project utilizes Tkinter to create a graphical user interface (GUI) that enables users to input data, select numerical methods, and visualize approximate solutions for first-order linear differential equations. Users can also compare solutions obtained via numerical methods with exact solutions generated using SciPy's `odeint` function and visualize absolute and relative errors.

## Features
### Data Input:
- **Manual Input**:
  - Enter the function f(dy/dt) in the format a*t+b or a*t, where a and b are constants.
  - Enter the initial value y0.
  - Enter the time interval in the format t_end,nr_steps.
  - Click "Save Data" button.
- **File Input**:
  - Click "Read Function from File" button.
  - Select a .txt file containing data in the correct format:
    ```
    f: a*t+b
    y0: value
    t: t_end,nr_steps
    ```
- **Random Data Generation**:
  - Click "Generate Random Function" button.

### Numerical Methods Selection:
- **Explicit Euler Method**
- **Implicit Euler Method**
- **Second Order Runge-Kutta Method**
- **Fourth Order Runge-Kutta Method**

### Visualization of Solutions:
- View approximate solutions on a graph using Matplotlib.
- Animation of the solution as it evolves over time.
- Comparison of numerical solution with exact solution.
- Display of absolute and relative errors for each time step.

### Data Management:
- Reset data and graph.
- Save animation as .gif file.

### Table Generation:
- Generate a table containing calculated numerical data for each time step.
- Display the table in a new window.

## Requirements
- Python 3.x
- Required Libraries:
  - tkinter
  - numpy
  - matplotlib
  - scipy
  - pandas
  - sympy
  - random
  - re

## Installation of Required Libraries
To install all required libraries, run the following command:

```bash
pip install numpy matplotlib scipy pandas sympy
```

## How to Use the Application

### Data Input
#### Manual Input:
- Enter the function f(dy/dt) in the specified format.
- Enter y0 and the time interval.
- Click "Save Data".

#### File Input:
- Click "Read Function from File".
- Select the .txt file with the required format.

#### Random Data:
- Click "Generate Random Function".

### Numerical Method Selection
Select one of the available numerical methods from the "Choose Method" section.

### Viewing the Solution
- Click "Start Animation" to begin the animation.
- Click "Stop Animation" to pause the animation.
- Click "Resume Animation" to continue the animation.
- Click "Show Table" to generate and display the numerical data table.
- Click "Save Animation" to save the animation as a .gif file.

### Resetting Data
- Click "Reset" to clear all data and the graph.

## Code Structure

### Calculation Methods
- `euler_explicit(f, y0, t)`
- `euler_implicit(f, y0, t)`
- `runge_kutta_2(f, y0, t)`
- `runge_kutta_4(f, y0, t)`

### Data Handling Functions
- `read_file()`
- `input_random_data()`
- `save_data()`
- `reset_data()`
- `calculate_absolute_error(y1, y2)`
- `calculate_relative_error(y1, y2)`
- `process_t(t, nr_steps)`
- `create_function(f_str)`
- `generate_table()`

### Animation Functions
- `start_animation()`
- `stop_animation()`
- `resume_animation()`
- `save_animation()`

### GUI Components
- Tkinter elements for data input and manipulation.
- Matplotlib elements for graph visualization and animation.
- Tkinter elements for displaying the numerical data table.

## Author
This project was developed to demonstrate various numerical methods for solving first-order linear differential equations and to provide an interactive interface for visualization and comparison of results.

