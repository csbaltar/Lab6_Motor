# Lab6_Motor
=========

## Basic Idea

controls a robot to go forward, backwards, left and right. 

## Set Up / Use

after connecting the robot, use each function to control the robot. 
For example, if you want the robot to make a left turn call these functions:

	forward();
	stop();
	bigLeft();
	stop();
	forward();
	
The functions can be used in a loop to repeat the movements.
Each function will go last for a certain period of time, so to move forward longer, call a function twice.

	forward();
	forward();

##Functions:

- 'void forward();'
	- moves the robot forward.

- 'void backwards();'
	- moves the robot backwards.
	
- 'void stop();'
	- stops the robot.
	
- 'void bigLeft();'
	- turns the robot left about 90 degrees.
	
- 'void bigRight();'
	- turns the robot right about 90 degrees.
	
- 'void smallLeft();'
	- turns the robot left about 25 degrees.
	
- 'void smallRight();'
	- turns the robot right about 25 degrees.