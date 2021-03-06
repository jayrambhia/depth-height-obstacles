Depth-Height-Extract
=====================

This repository contains codes for detecting obstacles and measuring their height and depth using Stereo Vision.

It does so, by matching points and calculation disparity between them. Further it calculates the homography
plane for these matched points and compares them with the previously calibrated ground homography.

To make it more foolproof, it uses Sonar Data as well on a connected microcontroller. 

In this case, the vision codes are running on Cubieboard and the Sonar data is on the arduino.

Both these are communicating using UART (ttyS2 port)

Codes for Serial communication, depth-height extraction and global variables are a part of this repo.

Following are the files and their description:

0. Makefile							- 		Make file for the folder
1. SerialUtilities.cpp 				-		Contains functions for serial communications
2. SerialUtilities.h				-		Header file for above
3. DepthHeightCalculations.cpp		-		Contains the main code for depth-height calculations
4. DepthHeightCalculations.h		-		Header file for the above
5. Globals.cpp						-		Initializes all Global parameters that are used in all the codes
6. Global.h							-		Header file for the above
7. cubieboard_serial_vision.cpp		-		Code containing the int main();
8. Arduino_Sketches/				- 		Folder containg the corresponding Arduino skecthes
9. rmaps.ymp						-		Data collected from the calibration code

### USAGE: 

Enter the folder and run make

    $ make

The excuetable will be named test. Just run the file.

    $ ./test

### ISSUES:
 - ADD CALIBRATION CODES
		
### Contributors:

 - Siddarth Biyani
 - Chirag Agrawal
 - Abhinav Gupta


