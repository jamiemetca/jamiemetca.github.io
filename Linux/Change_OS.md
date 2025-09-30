30/09/2025

# Changing OS

Documentation of steps to replace the operating system of a Lenovo Thinkpad T480

## Required tools
- Laptop
- USB drive
    - At leaset 5.9GB
- balenaEtcher
    - Or some other software to create the bootable drive

## Brieft steps
- Select OS
- Create a bootable USB drive with the new OS
- Restart and enter BIOS
- Boot from USB
- Install required drivers
- Have fun

## Steps
### Choose OS: Ubuntu
I have chosen a linux distrobution as my focus with this laptop will be development in the C programming language. I decided on Ubuntu as it has a large user base and hopefully plenty of resourses to help fix issues.

### Create bootable drive: > 5.9GB
The Ubuntu download is 5.9GB so I need a drive that can manage that
I'll need software to create the bootable drive.
balenaEtcher is suggested on ubuntu.com.

balenaEtcher works on windows so I might download it and prepare the drive with windows as this is what will come on the laptop.

### Restart and enter BIOS
As it says, restart the machine and enter the BIOS menu.
Change the boot order to prioritise the USB

### Boot from USB
Restart again and let the laptop boot from the USB
Follow any on screen prompts

### Install required drivers
Identify and install any required drivers.

### Have fun
See notes for setting up the toolchain to develop in C.
Write and run a "Hello world" C programm.