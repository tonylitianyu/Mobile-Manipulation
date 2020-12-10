Tianyu Li
ME449 Final Capstone

"overshoot" 

Feedforward-plus-PI Controller
Kp = 5.5
Ki = 1.0


The PI controller is done by manually commenting out the feedforward part in the control.py file.
In this case, small and overshoot oscillations happends at the beginning for each error curve (you might need to zoom in).
A large Kp with Ki will produce an overshoot and oscillation, which also causes a large velocity at the beginning as the video shows.

Joint limit is implemented for joint 3 to avoid self-collision and sigularity (always smaller than –0.2 rad or larger than 0.2 rad).
