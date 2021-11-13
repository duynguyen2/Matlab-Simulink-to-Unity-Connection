# Matlab/Simulink to Unity Connection
 
This is test code rebuilt from the Unity Link add-on from Simulink. The main thing to focus on is the Unity Connect Subsystem for how information is transferred and received.

The way it receives and sends data is in the subsystem, using TCP blocks. These will work asynchronously from each other. Feel free to mess with different data to send.
The function block in this subsystem is just an example used to format the camera module. It takes the data it receives, plugs it into a function that translates it into width and height, then sends that to the camera/video viewer. (Also requires another add-on in Simulink)

The test inputs is the data being sent to Unity. It tells it the positions (width and height for the camera, x, y, z, pitch, yaw, roll) of the camera. There is a sine step function which is meant to act as a variable position, so everytime the data is sent to Unity, the camera has a new position to displace.