# Mobile-Manipulation

Using a youBot mobile manipulator to perform a pick-and-place task for a cube by planning trajectory, performing feedback control, and calculating odometry. Joint limit is implemented to avoid self-collision and sigularity.

The code for this project cannot be made public. If you are interested, please email me for more details.

## Dependencies/Packages
```
modern_robotics
numpy
```

## Steps

1. Initialize youBot kinematics
2. Generate trajectory for the end-effector of the arm
3. Start simulation:  
  a. Calculate current state  
  b. Calculate control force for both joints and wheels using feedforward plus PID  
  c. Check joint limit  
  d. Update odometry  
  e. Repeat  
4. Plot
  
## Result

### Task 1
![task 1](task1.gif)

### Task 2
![task 2](task2.gif)
