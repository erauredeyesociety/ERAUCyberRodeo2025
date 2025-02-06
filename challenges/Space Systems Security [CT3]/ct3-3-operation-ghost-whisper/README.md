# [CT3] 3. Operation Ghost Whisper

## Description

![Challenge 3](/files/390e1f55c441ffa2d149644d735d0a20/challenge3.png)
The Github files referenced a WIFI network that supports the Ground Station locations. It's time to use one of the Aurora Alliance's capabilities against the Nebula Syndicate--an unmanned aerial system (UAS) with some secret sauce inside. The UAS (aka drone) can collect WIFI traffic and potentially learn more information on the dastardly Count Viktor Thunderclaw and the Nebula Syndicate.

One of the four Nebula Syndicate Space Laser Ground Stations was recently discovered by Aurora Alliance agents and the opportunity has been presented to use this specially equipped UAS platform to fly into uncharted territory and collect potentially sensitive signals.

On its route, the UAS will employ an automated version of the `aircrack-ng` suite of tools. It used airmon-ng to place its antennas into monitor mode, thus collecting all the 802.11 WIFI signals in the area. It simultaneously uses `aireplay-ng` to send deauthentication packets to the identified access points. As the clients attempt to rejoin their access points, their 4-way EAPOL handshake is collected.

The EAPOL (Extensible Authentication Protocol over LAN) 4-way handshake is a critical part of the security infrastructure for WPA2 (Wi-Fi Protected Access 2), which is used to secure wireless networks. This handshake process ensures that both the client device and the wireless access point have the correct credentials (such as a pre-shared key or passphrase), while also establishing encrypted communication between them.

#### **The attached video demonstrates the Aurora Alliance UAS collecting Wifi Packets**
 
------

Based on the collected Wi-Fi traffic, the intelligence team from the Aurora Alliance has determined that the Nebula Syndicate is using networks encrypted with WPA2. The BSSID identified as `nebula_syndicate` is of particular interest. To decrypt the traffic efficiently, the correct passphrase is required. Without it, one might resort to time-consuming brute-force attacks to crack the passphrase from the 4-way handshake. The collected traffic includes the associated EAPOL 4-way handshake between the client and the access point, allowing for the decryption of the packet capture using the passphrase (*if one could find it*) and the BSSID. Remember it's also been noted that the Nebula Syndicate relies on other insecure protocols, such as TELNET.

NOTE: You should not be connecting to any new wifi access points. Use the collected wifi .cap file to solve this challenge.

## Files

* [uas_wifi_dump.cap](<files/uas_wifi_dump.cap>)

* [c3_wifi_mission.mp4](<files/c3_wifi_mission.mp4>)

