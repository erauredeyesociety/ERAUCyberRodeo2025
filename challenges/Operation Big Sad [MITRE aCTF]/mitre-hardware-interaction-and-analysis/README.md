# [MITRE] Hardware Interaction and Analysis

## Description

The drone has been taken back to our workshop. If you can reverse engineer this drone, then we will know how all of the drones in this attack operate. Time is not on our side, reverse engineer this drone so we can put a stop to the Mastermind's plans before its too late!

**Objective:** Use an oscilloscope to determine the hardware architecture of the drone and identify which pinouts are transmitting valid ARINC 429 data.

**Instructions:** You will be provided with a custom hardware box used by the drone that has multiple pinouts. Your task is to use an oscilloscope to analyze the signals from these pinouts. Determine the hardware architecture of the box by examining the signal patterns and characteristics. Identify which pinouts are transmitting valid ARINC 429 data and which are not.

• NOTE: Familiarize yourself with the typical signal characteristics of ARINC 429, such as voltage levels, data rate, and bit encoding. 429 data is sent in paired pins that are in the inverse of each other.

• Document your findings on the hardware architecture and valid pinouts for future reference in the CTF.

**Tools Provided:** Oscilloscope, Probes and connectors for interfacing with the pinouts, and Documentation on ARINC 429 signal characteristics for reference.

**Example of valid message displayed on an oscilloscope here:** https://en.wikipedia.org/wiki/ARINC_429

![Pinouts](/files/MITRE/Pinouts)

Which pins are used to send ARINC 429 traffic? (Answer must be in ascending order seperated by commas) Example Input: "1,2,3,4,5"

