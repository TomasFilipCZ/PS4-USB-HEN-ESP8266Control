

<h1 align="center">PS4 USB HEN Controlled by ESP8266</h1>

<p>Small electronic board to support automatic loading HEN in PS4 with ESP8266. Project using method discovered on PS4 Firmware 9.00, where user need manually plug USB flash drive in right time to load HEN. 

Together with  ESP8266 as WebServer is PS4-USB-HEN  controlling power supply for USB drive, causing automatic loading HEN in desired time without user interaction.  

Project is modification of "PS4 Server 9.00", aim is to share design data of small PCB to create device for wide  usage of automatic loading and implement basic electronic protection for PS4.  </p>

<i>Status</i>
<b> 23.01.2022 waiting for PCB from production to add more picture and check design files !</b>

## Project requirements
- [ Wemos ESP8266 Mini Board ](https://www.wemos.cc/en/latest/d1/d1_mini_lite.html "v3.00") or any available clone supporting 4MB Flash, recommend is use version V3 with mounting holes as listed in pictures section below
- any working USB 2.0 Flash Disk ( size basically not matter >128MBytes, USB3.0 is not required)
-  Micro USB 2.0 data cable ( is recommend to not exceed length of 1.8M )

## Links
ESP8266 needs firmware to run WebServer with DHCP/DNS service, it can be found here:
- Either compile slight mod of PS4-Server-900 with USB Auto mount feature [PS4-Server-900u](https://github.com/stooged/PS4-Server-900u "<project-name>use pico-exfat")
or download binary file "ESP8266 Auto mount USB 900NA.bin"  from [compiled version by Karo (Twitter karo_sharifi ) ](https://t.co/9buavulD5x "900u.bin")
 

USB Drive for PS4-USB-HEN needs to be properly installed with ChendoChap Kernel Exploit 
- [ChendoChap PS4 9.00 Kernel Exploit](https://github.com/ChendoChap/pOOBs4 "pico-exfat")

## Setup
- Setup once USB Flash disk
Instructions can be found on ChendoChap PS4 GitHub or generally on internet, alternatively to Win32Disk Imager can be recommend [Rufus utility](https://rufus.ie/en/ "Rufus")   in both solution choose as USB Image  <b>exfathax_pico.img file</b>. 

- Setup once ESP8266
Either by Arduino IDE or [NodeMCU-PyFlasher](https://github.com/marcelstoer/nodemcu-pyflasher/releases), manual for programming ESP8266 with USB cable with PC can be find easily on internet. (with USB cable plug into ESP8266 board)

- Plug ESP8266 Board into PS4-USB-HEN, micro USB cable to PS4 and PS4-USB_HEN micro USB port. Due Webserver/DNS capability of ESP8266 web page with HEN  can be access through 'User Guide/Helpful Info' in PS4  <i>(required successful Wifi connection to ESP8266, if is not changed, access point is 'PS4_WEB_AP' , password is 'password' or '12345678</i> )

## Pictures
![PS4-USB-HEN v1.0b](/screenshots/PS4-USB-HEN_v10b.png)

![WeMos ESP8266 v3 with mounting holes](/screenshots/WeMos_ESP8266_v3.jpg)

![Bundle Ilustration (will be replaced with real picture)](/screenshots/bundle-ilustration.png)


## Project structure

- PCB Design data are developed in KiCad 5.1.10
- directory <b>bom</b> contains JLCPCB compatible BOM and BOM with MPN parts, including order codes from [TME.EU](https://tme.eu)
- directory <b>gerber</b> contains gerbers files with pick-up place file. Components are located only in TOP layer. USB A connector hasn't defined positions because is THT. 
- directory <b>libs </b> contains project specific  library special thanks to [ Raoul Rubien, for library for Wemos D1 Mini]( https://github.com/rubienr/wemos-d1-mini-kicad) and [ Fork Sand Devloper ](https://gitlab.com/forksand-dev1) for 3Dmodel of USB-A connector

## Future Updates

- [ ] Create STEP/STL Model of Plastic BOX to be able printed in 3D Printer
- [ ] Waiting for Delivering PCB to test all complete designs - <b> design is not tested YET! </b>

## Author

**Tomas Filip**

- [Profile](https://github.com/TomasFilipCZ "Tomas Filip on GitHub")
- [Join us on Discord](https://discord.gg/DWephJvzwR "Discord Server")

## 🤝 Support

Contributions, issues, and feature requests are welcome!

if you like this project, stay tuned !

<i>Special thanks: Karo, ChendoChap, stooged for their work and thanks to all community helper and developer on PS scene.  It's really fun...</i>
