# ESP8266 Deauther 2.0

<p align="center"><img alt="PICTURE logo" src="https://raw.githubusercontent.com/wiki/spacehuhn/esp8266_deauther/img/deauther_logo.png" width="200"></p>

<br>
<b>Scan for WiFi devices, block selected connections, create dozens of networks and confuse WiFi scanners!<br><br>
</p>

## What is New
  
Version 2.0:
- Completly rewritten code base for better performance and later enhancements
- Custom Deauther SDK for easy compiling using Arduino
- New serial command line interface to control and debug the program
- New display UI with a lot of new functions
- Improved web interface with multi-language support
- Improved scanning for access points and stations (+ continuous scanning mode)
- Save and select device names for both scanning and attacking
- Save up to 60 SSIDs and 25 devices in one list (you can create, load and save multiple lists)
- Added [PacketMonitor](https://github.com/spacehuhn/PacketMonitor) to display UI
- Deauth detection when scanning
- RGB LED support for a quick indication what the device is doing (attacking, scanning, ...)


## About this project
This software allows you to easily perform a variety of actions to test 802.11 wireless networks by using an inexpensive ESP8266 WiFi SoC (System On A Chip).  

The main feature, the deauthentication attack, is used to disconnect devices from their WiFi network.  
No one seems to care about this huge vulnerability in the official 802.11 WiFi standard, so I took action and enabled everyone who has less than 10 USD to spare to recreate this project.  
I hope it raises more attention on the issue. In 2009 the WiFi Alliance actually fixed the problem (see [802.11w](https://en.wikipedia.org/wiki/IEEE_802.11w-2009)), but only a few companies implemented it into their devices and software.  
To effectively prevent a deauthentication attack, both client and access point must support the 802.11w standard with protected managment frames (PMF).  
While most client devices seem to support it when the access point forces it, basically no WiFi access point has it enabled.  

Feel free to test your hardware out, annoy these companies with the problem, share this project and push for a fix!
This project is also a great way to learn more about WiFi, micro controllers, Arduino, hacking and electronics/programming in general.  
**But please use this tool responsibly and do not use it against others without their permission!**

The difference between deauthing and jamming: 
While a jammer just creates noise on a specific frequency range (i.e. 2.4GHz), a deauthentication attack is only possible due to a vulnerability in the WiFi (802.11) standard. The deauther does not interfer with any frequencies, it is just sending a few WiFi packets that let certain devices disconnect. That enables you to specifically select every target. A jammer just blocks everything within a radius and is therefore highly illegal to use.

## Official Deauther Boards

![PICTURE DSTIKE Deauther OLED Board](https://raw.githubusercontent.com/wiki/spacehuhn/esp8266_deauther/img/DSTIKE_Deauther_Board.jpg)


Those boards are optimized for this project, ready to use and come preflashed with the Deauther software!  

## Disclaimer
This project is a proof of concept for testing and educational purposes.  
Neither the ESP8266, nor its SDK was meant or built for such purposes. Bugs can occur!  

Use it only against your own networks and devices!  
Please check the legal regulations in your country before using it.  
I don't take any responsibility for what you do with this program.  

It is **not a frequency jammer** as claimed falsely by many people. Its attack, its method and how to protect against it is described above. It uses valid Wi-Fi frames described in the IEEE 802.11 standard and doesn't block or disrupt any frequencies.  

This project is meant to draw more attention on this issue.  
The [deauthentication](https://en.wikipedia.org/wiki/Wi-Fi_deauthentication_attack) attack shows how vulnerable the 802.11 Wi-Fi standard is and that it has to be fixed.  
A solution is already there, why don't we use it?

**Please don't refer to this project as "jammer", that totally undermines the real purpose of this project!**
If you do, it only proves that you didn't understand anything of what this project stands for. Publishing content about this without a proper explaination shows that you only do it for the clicks, fame and/or money and have no respect for intellectual property, the community behind it and the fight for a better WiFi standard!  

 

## License 

This software is licensed under the MIT License. See the [license file](LICENSE) for details.  
