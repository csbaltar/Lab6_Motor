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
	- 
	
##Example Code

'''int main(void) {
    WDTCTL = WDTPW | WDTHOLD;        // Stop watchdog timer


           TACTL &= ~MC1|MC0;            // stop timer A0
           TA1CTL &= ~MC1|MC0;

           TACTL |= TACLR;                // clear timer A0
           TA1CTL |= TACLR;

       TACTL |= TASSEL1;           // configure for SMCLK
       TA1CTL |= TASSEL1;

       TACCR0 = 50;                // set signal period to 100 clock cycles (~100 microseconds)
       TACCR1 = 25;

       TA1CCR0 = 50;                // set signal period to 100 clock cycles (~100 microseconds)
       TA1CCR1 = 25;

       TA0CCTL1 |= OUTMOD_7;
       TA1CCTL1 |= OUTMOD_7;        // set TACCTL1 to Reset / Set mode

       TACTL |= MC0;                // count up
       TA1CTL |= MC0;


       while(1){
                  forward();

                  stop();

                  backwards();

                  stop();

                 //forward();

                  smallLeft();

                  stop();

                 // forward();

                  smallRight();

                  stop();

                 // forward();

                  bigLeft();

                  stop();

                 // forward();

                  bigRight();

                  stop();
}
        
        return 0;
}'''
