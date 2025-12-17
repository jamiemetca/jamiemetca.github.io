[Back](./)

25/11/2025

# STM32CubeIDE

## Installation
- Install the ide from [here](https://www.st.com/en/development-tools/stm32cubeide.html)
- Make the the .sh file executable. [Notes here](/Linux/chmod)

```bash
chmod +x *.sh
```

I added executable permissons to all.


```bash
./ st-***.sh
```

Run the script.
I installed everything suggested.
And agreed to the agreements
 
## Power on
The board I bought came with example code to flash an onboard LED.
There is also a jumper clip between D2 ([CN3](/STM pin 5) and GND (CN3 pin 4).
Removing the jumper clip alters the speed at which the LED blinks.

TODO: Add video of "out of the box code, with jumper clip on and off.

The board comes with 

## First program
- File -> STM32 Project Create/Import -> STM32CubeIDE Empty Project
- Board selector -> nucleo-f04
    - This brought up the expected board
- Give it a project name
    - The next button didn't work for me after this and hitting enter seemed
to immediately create the project

