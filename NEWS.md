> # What's new #

**August 5**

Added I2C support. Now you can connect Port expanders, multichannel ADCs, Compasses, MCUs and so on.


**January 16**

Added functions for SD card files reading/writing
And the SD card areas (blocks) reading/writing



**2013**

**November 6**

Just added PWM\_out functions

Please watch the SCADA Video at:
http://www.youtube.com/watch?v=Q2mjBy_Yor4

**August, 5**

Added Sound to your projects
Look at: http://youtu.be/Qdtj17tCpfM


**July 12**

The Web Server/Client Projects posted


**June 20**

Connected to the Internet

Web Server is ready


**May 19**

SD card functions were improved. And no more need to format the SD card. Never!


**April 9**

Added Ethernet packets sending/receiving



**March 15**

Access to LCD screen buffer is open now!
Project Hello3 shows how to treat the buffer. Also how to make
User's custom Fonts for any language.
Having the address of the LCD buffer user can add his own Graphic/text functions.



**March 2**

Author may return FAT16 support - just let him know.
Users can work with Timer's Interrupts freely.
Please help by leaving feedback.



**Feb 16**

The system now supports FAT32 SD cards only. If some problems reading SD cards will arise, please report.
> Get\_mSeconds() was added.


> System works fast. Cold start (and your program too) **<1 second.**

> To launch the **screen calibration procedure:**
> - Tap the screen and hold the pen pressed at least 5 seconds

> No more counter of launches.

> With the proper SD card you can see up to 15 files on the menu screen.

> Some functions are in progress.

> One of them already present (for sliders, knobs, etc.)

> New touchscreen function:


> int 	Read\_TS	(U32 **x, U32**y);


> Usage:


int	pen\_down;	// You'll get pen status as funct() return

int	x;		// pen x will be placed here

int	y;		// pen y will be placed here

....	...	...	...	...

> pen\_down=Read\_TS(&(x),&(y));	// Put X,Y addresses and Read\_TS will fill them with X,Y

> if (pen\_down)
> {

...  ...  use x and y here

...  ...	...	...

> }

  * Hope see you soon...