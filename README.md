# Mobile-Manipulation

Using a youBot mobile manipulator to perform a pick-and-place task for a cube by planning trajectory, performing feedback control, and calculating odometry.

### Dependencies/Packages
```
modern_robotics
numpy
```

### Steps

1. Initialization youBot kinematics
2. Trajectory generation for the end-effector of the arm
3. Start simulation:
  a. Calculate current state
  b. Calculate control force for both joints and wheels using feedforward plus PID
  c. Check joint limit
  d. Update odometry
  e. Repeat
4. Plot
  


### Task 1
![task 1] (https://j.gifs.com/E8n2Yv.gif)

### Task 2
![task 2] (https://j.gifs.com/xnJBY9.gif)
