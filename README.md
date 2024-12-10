# Final-Project---Team-15
Project name - Alarm Clock Timer
Team members - Feng Tai, Mincheol Kim, Ziyuan Chu
Link to Project Demo Video - https://youtu.be/qcRieRde1qs?si=p5un-mbFgzh4Psfq
Overview of the Project - This project is a clock function with the capabilites of a manipulatable clock and a stopwatch. The stopwatch is able to be started and paused at any time along with the ability to be reset. The clock is able to be incrimented by 1 hour, miniute, or second. It is also a 24 hour clock so after 59 minutes or seconds those values will return to zero and after 23 hours, it will return to zero as well. This is linked to a VGA where the time will be displayed.
How to run our project - Open Vivado and download all the files. Program the FPGA with the overall top module and make sure it is connected to a VGA. 
overview of the code structure:
binary_clock - logic for alarm clock mode
timer - logic for timer mode
alarm_top - integrating binary_clock, vga_controller and pixel_generation(with rom)
timer_top - integrating timer, vga_controller and pixel_generation(with rom)
overall_top - integrating alarm_top and timer_top
vga_controller - diciding the coordinates of the pixels, generating horizontal_sync and vertical_sync
pixel_generation - output RGB to display graphics
rom - graphics for 0-9, A, T and colons
countdown_binary_clock - the same logic as binary_clock just counting backwards from a initial time set by the buttons (not fully functional)
EC311_Matlab - creates a real time clock value and gets it ready to export onto the FPGA
reciever - recieves the Matlab data through UART 
rtc - institaniate the reciever and manipulate the serial data to be used and displayed on the VGA (not fully functional)
constraints -buttons and switches on fpga corresponding to inputs

additional info - we don't have testbenches for our files, just implement them on fpga since all functions have been fully demonstrated.
