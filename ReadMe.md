![Physical ESP32 + LED strip configuration](ESP32 HyperHDR_scrubbed.png)
![Close up image of ESP32 wiring + LED strip wiring] (ESP32 HyperHDR Close Up_scrubbed)


ESP32 HyperHDR Lighting Controller

Overview
Custom-built ambient lighting system using an ESP32 microcontroller and HyperHDR to provide real-time reactive lighting based on screen output. This project integrates hardware wiring, firmware flashing, and network configuration.


Purpose
This project was built to:
- Learn microcontroller configuration
- Practice hardware + software integration
- Understand network-controlled devices
- Gain hands-on troubleshooting experience


Hardware Used
- ESP32 microcontroller
- Addressable LED strip
- 5v DC Power supply (my strip recommended 30amps, see how many LEDs you will use to use find the recommended AMPs)
- soldering gun + solder wire (or wire connectors)


Software Used
- Windows 11
- HyperHDR
- ESP firmware flasher 
- WLED controller firmware


System Architecture
PC → HyperHDR | Network | ESP32 | LED Strip


Setup Summary
1. Install the CP210x (ESP32 Model dependent) driver on Windows so that it can talk to/recognize the ESP32 once connected to the PC
1. Flash WLED firmware to ESP32
2. Connect the LED strip to the ESP32 pins (check the ESP32 model # to see your exact pin layout diagram)
4. Connect the LED strip to the 5v DC PSU
3. Configure the device on the network with the WLED software (it will be the IP address of the ESP32 on your network)
4. Connect HyperHDR to the ESP32 IP 
5. Set up the LED hardware LED layout (LED total count, orientation, maximum brightness)
5. Enable software screen grabbing in HyperHDR 


Network Configuration
- ESP32 connected via WiFi
- Static IP recommended
- Controlled via local network API


Challenges Encountered
Example:
- ESP32 not detected initially → fixed windows driver issue
- Connection drops → assigned static IP


Lessons Learned
- Importance of stable power delivery
- Firmware compatibility matters
- Network configuration is critical for IoT stability


Future Improvements
- Add enclosure
- Implement VLAN isolation for IoT devices
- Add an authentication layer
