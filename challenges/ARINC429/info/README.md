# Info

## Description

# ARINC 429
The ARINC 429 data transmission standard defines a layer two communication protocol in aircraft for transmitting digital information between avionics systems. ARINC 429 communications are simplex meaning that on a single channel, traffic flows from only one sending device to one or many receiving devices.

### ARINC 429 Word Format
ARINC 429 messages are called "words" and are 32 bits long.  The 8 least significant bits of each word denote the "label." The label identifies what data is being sent and is usually represented in octal.  Label 012, for example, indicates that the message is communicating the aircraft's ground speed.  The data field includes bits 11 through 29.  The ARINC 429 word also includes a source / destination identifier (bits 9 and 10), a sign / status matrix (bits 30 and 31), and an odd parity bit (32).  ARINC 429 words are often represented as a 32 bit hex string when stored.  ARINC 429 data can be encoded in a few different ways including in binary coded digits (BCD) and scaled binary (BNR).
<img src="https://i.imgur.com/RLVgvDz.png"/>

### ARINC 429 BCD Encoding
ARINC 429 Binary Coded Digits (BCD) encoding breaks up the data field into 5 decimal digits.  Digit one is represented the three most significant bits of the data (bits 27, 28 and 29).  Digits two through five are are represented by four bits each with digit two being represented by bits 23 through 26, digit three being represented by bits 19 through 22, digit four being represented by bits 15 through 18 and digit five being represented by bits 11 through 14.  The placement of the decimal point is based on the resolution of the data as defined in the label list.
<image src="https://i.imgur.com/hE6E2N8.png"/>

### ARINC 429 BNR Encoding
ARINC 429 Scaled Binary (BNR) encoding represents values in a scaled binary format.  The most significant bit (MSB) of the data field (bit 29) represents the sign.  A 1 in bit 29 indicates that the value of the data is negative and a 0 indicates that the value is positive.  The remaining bits of the data field (bits 11 through 28) contain the scaled binary data.  The MSB of the scaled data (bit 28) has a value of 1/2 of the maximum value of the range of the specific label.  Each bit descending in significance is then 1/2 of the previous (more significant) bit's value. For example, if the maximum value of the label was 100, then a 1 in bit 28 would represent 50.  A 1 in bit 27 would represent 25, bit 26 would represent 12.5 and so on.  Negative values are stored in twos complement meaning that every bit of the data except the sign bit and the least significant bit of the data (bit 11) are flipped.
<img src="https://i.imgur.com/RLVgvDz.png"/>

* () Accept

## Files

* [arinc429_label_list.pdf](<files/arinc429_label_list.pdf>)

