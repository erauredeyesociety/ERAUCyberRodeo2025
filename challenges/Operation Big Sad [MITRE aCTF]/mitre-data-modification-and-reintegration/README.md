# [MITRE] Data Modification and Reintegration

## Description

This is it. If you remove the frowny face from appearing, you will stop the attack. Use all the skills you have obtained so far and save all the cities from the swarm!

**Objective:** Modify the decoded data to transform a frowny face into a smiley face and load it back onto the SD card (ENCODED). Then you’ll need to jump the correct two pins with the correct voltage to initiate the SD load. 

**Instructions:** Take the decoded data from the previous challenge. Modify the data to change the frowny face into a smiley face or any other expression of your choice. Ensure that the modified data maintains the correct format and structure. Write the modified data back onto the SD card. Once you have uploaded your new image to the SD card you will insert it into the reading slot. To execute the upload from the SD card you must jump two pins on Terminal Block #2 at the correct voltage.

**NOTE:** This time the voltages are not provided to you and must be generated using the Raspberry Pi PICO provided to you. In order to load the file onto the SD card, the pins receive and alternating voltage every 2 seconds (2 Seconds LOW, 2 Seconds HIGH) from the PICO. Review wiring diagram for information on voltage.

**Tools Provided:** Text or binary editor for modifying the data, SD card reader/writer for transferring the modified data back onto the card.

**The flag will be given after display of team image.**


