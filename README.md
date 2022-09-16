# Robot Localization
## 2D histogram filter for estimating uncertainty from moving and sensing

### main.ipynb

- Visualizes the probability of the robot's local position (shown by the size of the blue circle).

### localizer.py

- Key functions in this histogram filter for localization.

- `initialize_beliefs()` - converts a 2D char vector to a 2D float vector containing initial probabilities

- `sense()` - the robot senses the color of the current grid point and calculates the resulting beliefs

- `move()` - move the robot by (x,y) and calculate the new beliefs

### simulate.py

- A `Simulation` class made up of functions to simulate and test the localization algorithm visually.

### helpers.py

- Other functions used to optimize localization.

- `blur()` - blurring parameter controls how much of a belief spills out into adjacent cells.

- `normalize()` - computes the correspond normalized version of that grid

- `is_robot_localized()` - robot has a strong opinion when the size of it's best belief is greater than twice the size of its second best belief
