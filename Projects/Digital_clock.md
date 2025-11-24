24/11/2025

# Digital clock

The aim is to build and write up lots of small project, which all work towards
the overall project of building a clock.

With no limitiations this will be a digital clock which sets it's own time via
the MSF radio signal.
The user will be able to adjust the time via some interface (buttons).
The user will be able to set an alarm
The clock alarm will be both visual and audible.

The mantra of this project is baby steps.
What's the bare minimum I can do and still incrementally learn something.

Steps (not ordered)
- [] Download STM32CubeIDE
    - [] Run a basic project (blinky)
- [] Read and make notes on the board's documentation
- [] Intergrate with other components
    - [] Flash an external LED
- [] How to use a display
    - [] Review 4 bits seven segement display
    - [] Review LCD display
- [] Investigate and document the boards RTC (real time clock)
- [] Count with the board
    - [] Increment counter a display it
    - [] Increment the time and display it
Extra points
- [] Detect the MSF radio signal (auto-set)

## STM32CubeIDE
- How to install
- How to get a basic example project onto the board
- How to write bespoke code and get it on the board
- HDL - What are some of the basic things to help get up and running

## RTC real time clock
Investigate and document the RTC.

### Counting with an RTC
Get the RTC working Whatever that means.

Using the internal low-speed ocillator.  Ideally increment a counter every second

### Counting in hours minute and seconds using the RTC
What's the best way to keep track of human readable time?
Investigate and write up notes.

### Counting with an external low-speed external crystal (LSE)
- What is this?
- How do I use one?
- Do I need one?

## Time Display
Which display is the easiest to use.

### 4 digits 7 segment
    - How does it work?
    - pros and cons
    - Write up documentation
### LCD display
    - How does it work?
    - pros and cons
    - Write up documentation

## Buttons
Use buttons

### Detect button press
Adjust the count/time with a button press

### Handle more than one button
Eventually the clock will most likely need more than one button.
How can I handle more than one button?
