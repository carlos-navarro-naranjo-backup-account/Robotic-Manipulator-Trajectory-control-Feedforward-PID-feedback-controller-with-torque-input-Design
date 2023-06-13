# Robotic-Manipulator-Trajectory-control-Feedforward-PID-feedback-controller-with-torque-input-Design
Robotic Manipulator Trajectory control / Feedforward PID feedback controller with torque input Design Mechanics of Robotic Manipulators Graduate Research Project  
## Problem Statement & Goal:
![image](https://github.com/carlos-navarro-naranjo-backup-account/Robotic-Manipulator-Trajectory-control-Feedforward-PID-feedback-controller-with-torque-input-Design/assets/134238682/119cd61a-93eb-4455-9e85-b9b9c2b7e528)

For this project I considered an RR manipulator in its zero configuration, as shown above, with 𝐿1 = 3 and 𝐿2 = 2. My robot has a marker attached at the end-effector, which can draw on the board defined by the x-y plane. I was tasked to control the robot to draw a straight vertical line from (2, 3) to (2,0) within 3 seconds. The desired trajectories in the task space are given by:
1.	I generated the desired positional trajectory (𝜃⃗𝑑) in the joint space numerically by using the Newton-Raphson method. Plots of the joint trajectories in a single graph, with 𝑡 along the x-axis and 𝜃1(𝑡) and 𝜃2(𝑡) on the y-axis can be shown in the report as Figure 1. I also plotted the calculated end effector trajectory given calculated 𝜃1(𝑡) and 𝜃2(𝑡) saved as Figure 2. 

▪ For each figure, I used different colors & line types for individual variables. ℎ = 0.1 [sec] was chosen for the time step size and ed = 0.001 for the desired error. 

▪ For the Newton-Raphson method, I used the initial guess 𝜃⃗(0) 0 = [ 𝜋/ 6 , 𝜋/6 ] 𝑇 ; and for all following data point I used the previously calculated 𝜃⃗ values as the initial guess for the next approximation, such that 𝜃⃗(𝑡𝑖 ) 0 = 𝜃⃗(𝑡𝑖−1 ) 𝑛 , where 𝜃⃗(𝑡𝑖−1 ) 𝑛 is the final approximation at the previous time step. 

2.	Now, I was tasked to  consider a constant speed control with the desired trajectory specified by 𝜃⃗𝑑 = [𝑡, 0] 𝑇 ; 𝜃⃗ dot  𝑑 = [1,0] 𝑇 , 𝑎𝑛𝑑 𝜃⃗dot dot 𝑑 = 0⃗.  If the center of mass for each link (considered as a point mass) is located at the distal tip of the link, and there is no friction. In this case, the dynamic model of this robot can be calculated as

![image](https://github.com/carlos-navarro-naranjo-backup-account/Robotic-Manipulator-Trajectory-control-Feedforward-PID-feedback-controller-with-torque-input-Design/assets/134238682/7fde1b1e-5bdd-4c84-94b8-73ab4f417918)

Where:

![image](https://github.com/carlos-navarro-naranjo-backup-account/Robotic-Manipulator-Trajectory-control-Feedforward-PID-feedback-controller-with-torque-input-Design/assets/134238682/f9c59f83-9cbd-4361-97bc-fe327b2533e9)

given 𝑚1 = 𝑚2 = 1𝑘𝑔, and 𝑔 = 9.8𝑚/𝑠 2 . 

a)	My task was to Design the feedforward plus PID feedback controller with torque input using 𝑘𝑝 = 10, 𝑘𝑑 = 5, and 𝑘𝑖 = 0.2 for both joints. 

b)	Using MATLAB, I plotted the torque 𝜏1 and 𝜏2 obtained from the controller for t = 0: 0.1: 5[sec]. I used different colors or line types for 𝜏1 and 𝜏2 and saved it as Figure 3.
 
c)   Using MATLAB, I plotted 𝜃1(𝑡) and 𝜃2(𝑡) for where 𝜃1(0) = 1 and 𝜃2 (0) = 1 by    numerically integrating the acceleration resulted from the PID controller and saved it as Figure 4.

## Concepts learned while working in this project:

•	rigid-body motions, forward and inverse kinematics, differential kinematics, forward and inverse dynamics of robotic manipulators, motion planning, and control theories

•	Assign frames of reference to mathematically describe the locations of individual joints and end-effectors of the robot.

•	Understand the relationships between kinematic design, configuration space, and workspace.

•	Describe the dynamic motions of a robotic manipulator and apply analytical and/or numerical methods to solve the equations of motion.

•	Apply linear control laws for controlling a robotic manipulator with a single or multiple degrees of freedom.

