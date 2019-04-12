# Testing the proof of concept

This  testing  scheme  eliminates  the  need  to  procure  a  realvehicle, and mitigates risks associated with testing in the real world.

The Arduino was programmed to simulate an ECU by incorporating the following functions:
1. Respond to standard OBD-II parameter queries, such as returning a randomly generated vehicle speed
2. Indicate normal vehicle operation through a green LED
3. Perform an action (turn on a red LED) when receiving specific CAN packets to demonstrate vehicle immobilization

This code is located in `testing/software/Signal_Read_and_Write/Signal_Read_and_Write` in the .ino file.

After flashing this code on to any Arduino Uno, connect said Arduino to the CAN controller/transceiver circuitry described in `testing/hardware`. 
Connect the CAN HI/LO from the CAN Transceiver to the CAN HI/LO of the proof of concept device to establish communication between the two modules.
