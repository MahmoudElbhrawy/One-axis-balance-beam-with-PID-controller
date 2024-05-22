# One-axis-balance-beam-with-PID-controller

A proportional–integral–derivative controller (PID controller) is a control loop feedback mechanism commonly used in industrial control systems. A PID controller continuously calculates an error value e(t) as the difference between a desired setpoint and a measured process variable and applies a correction based on proportional, integral, and derivative terms (sometimes denoted P, I, and D respectively) which give their name to the controller type.

We will use this mechanism to control some brushless motor in order to calibrate our drone. We will put the motors on a balance and calculate the angle using the MPU6050 or the MPU9250 IMU module. So in our case the value that we will contro is the inclination angle of our drone. The e(t) error will be the difference between the raal angle of the drone and the desired one. The desired one will be 0, which means taht the drone is perfectly horizontal.

Each brushless motor will have a different power for the same PWM signal because motors are not perfect and they will never be the same. Fot that we have to constantly measure the angle of our drone, compare that value with the desired value and rectify the error if there is one.

So to tune our motors we will first build a balance for just 2 motors. This two motors represent just one axis, in this case will be the x-axis. As you know a drone can move in any of the 3D axis, x,y and z. All we want to do with this balance is to find our P, I and D constants. Each of this 3 constants will affect in one way or other the entire PID control, and we have to find the perfect ones.

Circuit Diagram
![WhatsApp Image 2024-05-22 at 22 05 35_eefd2ffc](https://github.com/MahmoudElbhrawy/One-axis-balance-beam-with-PID-controller/assets/110239321/9f86c473-2951-424e-8210-4303c75e98af)

