# [CT3] 4. Operation Signal Storm

## Description

![Challenge 4](/files/8687f84fad215577daaa055976866bec/challenge4.png)
After confirming WPA2 access by analyzing UAS packet captures, the Aurora Alliance has tactically placed a rogue wireless client in the field and joined the Nebula Syndicate Network. The Nebula Syndicate's lack of MAC address validation or certificate-based authentication like 802.1X allowed for seamless WIFI network access. This rogue device was discreetly installed adjacent to a previously surveilled ground station. Through this stealthy connection, your team has established an encrypted tunnel, providing network access not only to the ground station network but also to the expansive Nebula Syndicate Network, including the Administrative/Evil Network and the Mission Operations Center (MOC).

Ground station antennas sometimes utilize a complex collection of systems to automate the effective tracking and communication with satellites. Key subsystems include antenna drive systems, servo control systems, advanced beamforming networks (particularly in setups with phased array antennas), tracking receivers and processors, feed systems and low noise amplifiers (LNAs), frequency converters and filters, as well as control, monitoring, and environmental control systems (ECS).

![NSN](/files/0b974cbc78708cda49c3212a40573dbf/nebula_syndicate_network.png)
![Nebula Wifi](/files/f2436920a8e3a8f4e0e87d08015fac32/nebula_wifi.png)

Our mission is to wreak havoc on the ground station antenna, crippling the Nebula Syndicate's ability to track and control their Space Laser Satellite. Our primary target will be the Antenna Drive System—a motorized setup responsible for the antenna's movement. This system enables both azimuth (horizontal) and elevation (vertical) adjustments, allowing for precise tracking of satellites across the sky. These movements are critical for maintaining a continuous lock on fast-moving targets, especially for Low Earth Orbit (LEO) satellites like the Nebula Syndicate Space Laser.

Often, these ground stations operate on embedded software or Real-Time Operating Systems (RTOS). However, due to severely constrained budgets—where the IT staff must metaphorically search through couch cushions for funding—IT priorities are often neglected. As a result, the Nebula Syndicate has opted for a low-cost, readily available tracking software, SatPC32, which they have modestly adapted for their specific needs. This particular version of SatPC32, running on Windows, is notably deficient in crucial security features, such as user account controls. This lack of robust security allows for unrestricted access through its graphical user interface.

The Aurora Alliance's plan? Disrupt the Rotator Controller to throw their tracking capabilities into disarray. Check out the video and then use the flag below to proceed to the next challenge:

Flag: `ct3_flag_69732d69742d726f6775652d6f722d726f7567653f`

