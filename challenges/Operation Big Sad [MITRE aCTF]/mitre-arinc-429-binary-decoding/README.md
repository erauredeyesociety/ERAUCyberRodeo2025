# [MITRE] ARINC 429 Binary Decoding

## Description

**Objective:** Decode the ARINC 429 binary messages. Background information has been included below.

**What is ARINC 429?**
Aeronautical Radio INC (ARINC) is a standard for local area networks for commercial and transport aircraft. It allows communication between various avionics systems aboard the aircraft, each providing services including communications, guidance, altitude reference, and flight management.

The ARINC 429 bus is unique in its use of a simple uni-directional flow of bus data. A single uni-directional channel is composed of a differential pair, where each line carries an equal and opposite voltage to reduce noise. ARINC 429 hardware consists of a single transmitter source that can support
up to 20 receivers. For multidirectional communication, differential pair is required for data transmission in each direction.

ARINC 429 data words are 32 bits that are broken down into several parts. The first 8 bits are a label that describes the data that is being transmitted. The remaining 24-bits contain the core information. When a data transfer occurs, bit 1 is transmitted first and bit 32 is transmitted last. Note that bit 1 of is the most-significant bit of the label and bit 8 is the least-significant bit.

![ARINC429WordFormat](/files/MITRE/ARINC429WordFormat)

**P -** Parity Bit - Used for error detection – Bit 32
**SSM -** Signal/Status Matrix - Indicates sign or direction – Bit 31-30
**Data -** Actual data that is being transmitted – Bit 29-11
**SDI -** Source/Destination Identifier - Used by a transmitter to identify which receiver should process the message – Bit 10-9
**Label -** Identifies the type of information contained in the word. – Bit 8-1

Documentation Links:

ARINC Documentation for Labels: http://toddheffley.com/wordpress/wp-content/uploads/2014/07/Arinc429WordList-copy.pdf

ARINC Decoding Examples for Labels: https://www.aim-online.com/wp-content/uploads/2019/07/aim-tutorial-oview429-190712-u.pdf

**Instructions:** You will be provided with a series of ARINC 429 binary messages. Each message, when decoded, will reveal a piece of critical information. The decoded information will be essential in helping to prevent the attack. Note: assume Equipment ID’s of 004, 056, and 00B and that each full word is in big-endian format.

**We have knowledge that the Mastermind may be nearby. One of the drones has been discovered at a discrete location. Along with the drone was a folder containing some encoded messages.**

* () Accept

## Files

* [Challange_1_traffic_four_words.json](<files/Challange_1_traffic_four_words.json>)

