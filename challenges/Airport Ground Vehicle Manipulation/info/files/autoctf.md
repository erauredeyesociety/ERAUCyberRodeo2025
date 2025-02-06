auto.md 2024 - 04 - 13

```
1 / 2
```
# Automotive Inspection

## Setup

```
Login: competitor
Password: competitor
```
```
0. Open two Terminals
1. Load setup_vcan.sh
```
```
> cd /home/competitor/ICSim
> ./setup_vcan.sh
```
```
2. (Terminal 1) ./icsim vcan
```
```
> cd /home/competitor/ICSim
> ./icsim vcan
```
```
3. (Terminal 2) ./controls vcan
```
```
> cd /home/competitor/ICSim
> ./controls vcan
```
## Using the Tools

```
0. CanSniffer
```
```
> cansniffer [options] vcan
```
```
To have the best viewing experience of all CAN IDs, make the terminal as tall as possible.
1. CanSend
```
```
> cansend vcan0 [id]#00...
```
```
Sends CAN messages
2. CanDump
```
```
2 / 2
```
```
> candump [options] vcan
```
```
Logs can files into a log file
3. CanPlayer
```
```
> canplayer [options] vcan
```
```
Replay logged file
```
## Controls/Keybinds

```
Your window must be focused on the controller window.
For indicators and acceleration, it is best to hold down the key.
Indicators - Right/Left Arrows
Accelerate - Up Arrow
Right Shift + A - Unlock Driver Front
Right Shift + B - Unlock Passenger Front
Right Shift + Y - Unlock Passenger Rear
Right Shift + X - Unlock Driver Rear
Left Shift + A - Lock Driver Front
Left Shift + B - Lock Passenger Front
Left Shift + Y - Lock Passenger Rear
Left Shift + X - Lock Driver Rear
Hold Shift Left + Right Shift - Unlock All
Hold Shift Right + Left Shift - Lock All
```

```
2/2
```



# Instruction Manual: Converting CANBUS (Hex) Values to Engine RPM 

## Introduction 
```
In this challenge, you will learn how to convert CANBUS data values to a car engine's RPM (Revolutions Per Minute). RPM is an essential measurement in automotive engineering, as it tells how fast the engine's crankshaft spins. 

We’ll guide you step-by-step through interpreting the hex value and calculating the corresponding RPM. 
```

## Definitions 
```
> Hexadecimal (Hex): A base-16 number system using the digits 0-9 and letters A-F. 

> RPM (Revolutions Per Minute): The number of complete turns the crankshaft makes in one minute. 

> CANBUS data values: a set of hex values with an arbitration ID that corresponds to any given sensor or light. 

> ECU (Engine/Electronic Control Unit) – A computer in a vehicle that manages and controls various electronic systems, such as engine performance, transmission, and safety features, by processing data from sensors and executing commands. 
```

## Step-by-Step Guide 
```
Step 1: Understanding the Input 

The ECU often outputs sensor data in hexadecimal format. For this challenge, you are given a CANBUS data output sample and the information from the vehicle's manufacturer's DBC (CAN Database) file. 
```
```
Example: 

The ECU output is ID:186 (engine rpm) DATA:0x00 42 35 20 45 00. 
```
```
Step 2: Convert the second and third bytes to Decimal 

Hexadecimal numbers must first be converted into decimal numbers (base-10) to be meaningful in terms of RPM. 
```
```
Convert the hex value 0C1F to decimal: 

> 42 35 in hex = 16949 in decimal 
```
```
Step 3: Use the Formula for RPM Calculation 

The ECU provides the engine speed in a format where the decimal value must be multiplied by a scaling factor to get the RPM. The scaling factor may vary depending on the ECU or specific vehicle, but for this challenge, the scaling factor is .125
Use the formula: 

RPM = Decimal Value * Scaling Factor 
```

## Our example 
```
RPM = 16949 * .125 = 2118.6  

Thus, the engine is running at approximately 2118.6 RPM. 
```
```
Step 4: Verifying your result after performing the conversion, verify that the RPM value makes sense for the context of the car's engine. For example, most engines idle at 600-900 RPM and can rev up to around 6,000 to 8,000 RPM under heavy load. 
```

## Hints
```
> Use the same steps as outlined above.  

> Remember to multiply by the scaling factor of .125. 
```

## Troubleshooting 
```
- Incorrect Decimal Conversion: Make sure to convert hex values into decimal correctly. 

- Wrong Scaling Factor: Check that you use the correct scaling factor for your vehicle/ECU. 
```

## Conclusion 
```
Following these steps, you can accurately convert hexadecimal ECU outputs into meaningful RPM values for a car engine. This skill is crucial in automotive diagnostics and data interpretation. 
```