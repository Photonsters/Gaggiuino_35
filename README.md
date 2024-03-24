# Gaggiuino Nextion display HMI files

by Steve Nofs

See the latest demos on [youtube](https://www.youtube.com/@stevenofs8795).

## NEXTION 3.5" DISPLAY and NEXTION 2.4"/2.8" DISPLAYS

### How to use
1.  Open in Nextion editor, click the "Device ID" in the top menu bar, select your Device. 
2. Select "Display" and choose rotation: select 270 for Robert Silvers 3.5" bezel.


### NEXTION 2.4" and 2.8" DISPLAY 
For Nextion 2.4" and 2.8" screens.

Open in Nextion editor, click the "Device ID" in the top menu bar, select your Device. Then select Display and choose rotation: select 90 for the original 2.4" or select 270 for Robert Silvers 2.8 bezel".

Then select FILE/TFT OUTPUT and save to a microSD card to flash the display.



##### Nextion 2.4"/2.8" Version History #####

#### Ver. 24MAR2024:

- Full rework of Manual Brew Screen with Brew Graph, Flow, Flow Target, Weight, Target Weight, Shot Hydaulic force feedback gauge during shot.
- Realign/organize components in Brew Settings screens.
- Color code data entry components in Brew Setting screens: Weight=GREEN, Flow=YELLOW, Temperature=RED, Pressure=BLUE.
- Added Target Weight to Brew Screen
- Added target weight to Brew Screen

#### Ver. 10MAR2024:
- A better indication of Stop-on-weight being enabled: red outline on the button with white text; easier to read. 
- LED configuration screen to configure LED color
- Added background color to water level gauge for better visual.
- Fine-tuned alignment of graphic elements on Home screen.



##### Nextion 3.5" Version History #####

#### Ver. 24MAR2024:

- More cleaning up of Brew option screens; aligning/arranging components
- Added Preview button to Soak Screen

#### Ver. 21MAR2024:

- Full rework of  Manual Mode.
- Added ShotPower meter: this is an indicator of the hydraulic force applied to the puck


#### Ver. 06MAR2024:

- Added functional code to the LED color configruation screen.
- LED ON/OFF not functional; turn LED off by setting RGB to zero.
- For anyone interested here is how one reads the LED settings:
```
LED_ON=ledNum&0x02000000>>25
LED_DISCO=ledNum&0x01000000>>24
LED_RED=ledNum&0x00FF0000>>16
LED_GREEN=ledNum&0x0000FF00>>8
LED_BLUE=ledNum&0x000000FF
```

Save updated values like this:

`ledNum=bt0.val<<1+bt1.val<<8+n0.val<<8+n1.val<<8+n2.val`


#### Ver. 02MAR2024:
- Matched original Left-to-Right brew graph format and speed
- Adjusted brew graph vertical lines at 10 seconds per line
- Weight button on main screen gets RED outline when Stop-on-dose is enabled


##### Ver. 14FEB2024:
- Weight button text on main screen is RED when Stop-on-dose is enabled
- Started cleaning up Brew Preview screen


#### Ver. 29JAN2024:
- Added Temp and Pres mini-graphs to main screen
- Added graphical buttons across top of main screen
- Standardized colors where possible: 
    - RED/Temp
    - BLUE/Pres
    - YELLOW/Flow
    - GREEN/Weight


#### Ver. 22JAN2024:
- Basic beginning of 2.4 --> 3.5 conversion



### Need help or have Feedback?
- [Gaggiuino Builders on FB](https://www.facebook.com/groups/5362374853865845)
