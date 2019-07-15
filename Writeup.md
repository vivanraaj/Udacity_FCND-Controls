# Writeup #

The main codes which were added are in src/QuadControl.cpp and the tunable PID parameters are in config//QuadControlParams.txt.

## Criteria ##


### 1.Implemented body rate control in C++ ###
The goal of this criteria is to ensure the rotation of the quad gets controlled to 0. The function 'GenerateMotorCommands()' & 'BodyRateControl()' 
is tweaked at lines 78-87 &  111-116.


### 2. Implement roll pitch control in C++. ### 
The quad mass is taken into account for body rate command. These features are added to the function  'RollPitchControl' in lines 145-168.


### 3. Implement altitude controller in C++. ### 
The function 'AltitudeControl()' is tweaked 
to ensure the thrust commanded include the non linear effect from non-zero roll/pitch angles.These features are added in lines 198-214.

### 4. Implement lateral position control in C++. ###
The function 'LateralPositionControl()' is tweaked 
to ensure drone uses the local position and velocity to generate the desired acceleration. These features are added in lines 251-273.


### 5. Implement yaw control in C++. ### 
The function 'YawControl()' in lines 298-313 enables the quad to go to the destination point with greater yaw control to ensure its badly tilted.

### 6. Implement calculating the motor commands given commanded thrust and moments in C++. ### 

I added integral term in the controller for AltitudeControl and LateralPositionControl.


### 7. Your C++ controller is successfully able to fly the provided test trajectory and visually passes inspection of the scenarios leading up to the test trajectory. ### 

The drone is able to completely pass the test scenario for the trajectory.