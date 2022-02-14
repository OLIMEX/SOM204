SOM204-EVB is evaluation board for the OLIMEX's SOM204 modules.

The EVB board has all features exposed so it can be used as a template for creating own designs. The design was made with Eagle CAD version 4.16r2.

Notable hardware revision changes:

Revision C2
=========
1. Changed the CAN chip. U2 now SIT1042T/3(SOIC-8_150mil), previously MCP2562-E/SN(SOIC-8_150mil) ;

Revision C1
=========
1. Added C79 capacitor 10uF/10V/10%/X5R/C0603 in parallel to the EVB's RESET button. AXP is held in reset for approximately 10ms after power-on.

Revision C
========
1. R104/R105/GPIO11/HP-DET group was moved from HEADPHONES/LINEOUT pin<4> to HEADPHONES/LINEOUT pin<1>!
2. R95/R98/GPIO10/MIC-DET group was moved from MIC/LINEIN pin<4> to MIC/LINEIN pin<1>!
3. One NA resistor (R127) was added between HEADPHONES/LINEOUT pin<1> and MICINL/LINEINL.
4. Improvements around the USB-HOSTs:
	-> R125 changed from 6.81k/1%/R0603 to 3.9k/1%/R0603, thus the current limiter was changed from 1000mA to 1744mA.
	-> R134 changed from 13k/1%/R0603 to 3.9k/1%/R0603, thus the current limiter was changed from 523mA to 1744mA.
	-> R122 changed from 13k/1%/R0603 to 6.81k/1%/R0603, thus the current limiter was changed from 523mA to 1000mA.
	-> R131 changed from 49.9k/1%/R0603 to 51k/1%/R0603, thus the step-up voltage output is lifted up from 5.0V to 5.1V.
	-> FB0805 remain as they were, i.e. not shortened. If someone has got any problems this could be done.
5. USB_MICRO_3.0-AB connector amd corresponding components, moved 40 mils.
6. U.FL_Connector, by defalut: NA, added to the WiFi/BT module to enable option for external antenna. R139 = 0R/0402 added in series to the PCB antenna because of this.
7. In the Platform's value added [2*(KF02S-M2)].
8. U2 changed from MCP2551-I/SN(SO8) to MCP2562-E/SN(SO8). Because of this: 
	-> R14 was changed from NA/R0603 to 0R/R0402(The same package like R139 for to reserve a feeder). 
	-> R13 was changed from 2.2k/R0603 to NA.
	-> R11 was changed from 1.05k/1%/R0603 to 100R/R0603.
	-> R2 was changed from NA to 100R/R0603.

Revision B1
=========
1. The C79 capacitor 1uF/10V/10%/X5R/C0603 was added in parallel to the EVB's RESET button. Thus AXP is hold in reset for approximately 10ms after power-on.
   This solves the problem with AXP209's refuse to start up when 5V external power supply is applied! 
   This is the patch which will be made over all the boards from Rev_B. This will solve the problem at all earlier versions also.

Revision B
=========

Initial board release
