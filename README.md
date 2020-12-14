# Mobile-Manipulation

In the coppeliasim, using a youBot mobile manipulator to perform a pick-and-place task for a cube by planning trajectory, performing feedback control, and calculating odometry for the omnidirectional wheels. Joint limit is implemented to avoid self-collision and sigularity.

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


## youBot Kinematics
- Omni-directional mobile base  
  ![](http://hades.mech.northwestern.edu/images/thumb/c/c8/Yb-base-capstone.png/300px-Yb-base-capstone.png)  

- Arm  
  - Dimension and frames  
    ![](http://hades.mech.northwestern.edu/images/thumb/3/33/Yb-book.png/500px-Yb-book.png)  
    ![](http://hades.mech.northwestern.edu/images/math/c/9/0/c9032f3f6bf50c6f77853b04e3c2b542.png)  
    ![](http://hades.mech.northwestern.edu/images/math/3/f/b/3fb287b1dcc4d719b721791e3fb1da6e.png)  

  - Screw axes with home configuration  
    ![](http://hades.mech.northwestern.edu/images/math/e/6/8/e680119b43afbf48ddfe3e328318c260.png)  
    ![](http://hades.mech.northwestern.edu/images/math/a/a/2/aa219a0a08e4b12ffdd065fe79f6327c.png)  
    ![](http://hades.mech.northwestern.edu/images/math/7/3/3/7332314e1692adee49e7f1fb55681c80.png)  
    ![](http://hades.mech.northwestern.edu/images/math/9/1/7/9179792f7910beaef1c9c63ca4265eaa.png)  
    ![](http://hades.mech.northwestern.edu/images/math/8/d/a/8da1051514f4c3f02549d7e48ac0cdb8.png)  
    ![](http://hades.mech.northwestern.edu/images/math/0/4/c/04cc86c9414c537fca1680d5e6291d48.png)

## Odometry

- Wheels  
    <img src="https://render.githubusercontent.com/render/math?math=u_{new} = u_{old}%2B\dot{u}*\triangle t">  

- Arm  
    <img src="https://render.githubusercontent.com/render/math?math=\theta_{new} = \theta_{old}%2B\dot{\theta_{joint}}*\triangle t">  
    
## Control

   ![](http://hades.mech.northwestern.edu/images/math/9/a/0/9a032c056fee4a288c16a2c17c00c319.png)  
   ![](http://hades.mech.northwestern.edu/images/math/1/0/a/10ac484b01fdec266f2b9ec30cdea54d.png)  
   ![](http://hades.mech.northwestern.edu/images/math/1/a/b/1ab4bf8959a0d15c78ad497ba742276f.png)


  
## Result

### Task 1

Demo:  
<img src="task1.gif" width="800"/>

Error twist:   
<img src="best/Xerr_plot-1.png" width="800"/>


### Task 2

Demo:  
<img src="task2.gif" width="800"/>

Error twist:  
<img src="newTask/Xerr_plot-1.png" width="800"/>


## Image Credit and Reference

http://hades.mech.northwestern.edu/index.php/ME_449_Robotic_Manipulation
