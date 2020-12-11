# Mobile-Manipulation

In the coppeliasim, using a youBot mobile manipulator to perform a pick-and-place task for a cube by planning trajectory, performing feedback control, and calculating odometry for the omnidirectional wheels. Joint limit is implemented to avoid self-collision and sigularity.

The code for this project cannot be made public. If you are interested, please email me for more details.

## Dependencies/Packages
```
modern_robotics
numpy
```

## Steps

1. Initialize youBot kinematics （Please refer to the Modern Robotics textbook exercise 13.33 for details)
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

Demo:  
<img src="task1.gif" width="800"/>

Step response for error twist:   
<img src="best/Xerr_plot-1.png" width="800"/>


### Task 2

Demo:  
<img src="task2.gif" width="800"/>

Step response for error twist:  
<img src="newTask/Xerr_plot-1.png" width="800"/>
