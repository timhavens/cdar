|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

**"Why would I want a GPS connected to a radio?"** you might be asking yourself.  GPS can be used for MANY things, not simply global positioning, and tracking where you are on Earth.  There is also the ability to use the GPS clocks as a local **stable** 10Mhz oscillator frequency source.

  * This means that the radio can be spot on frequency every time.
  * It also means that we transmit and receive echo's of transmissions that are 'timestamped' which can help to verify how long the transmitted chirp takes to echo return to the receiver.  This is a requirement for accurate "bistatic radar echo timing" used in determining the distance to the reflection point of the echo.
  * It also means that if other people are listening for echos on the same frequency that they can be positive that they're logging an ECHO and not the original transmission.
  * It also means that if other people are listening they will know exactly **WHEN** to listen, and even 'blank' the original transmission and only hear ECHOs!

## Useful Software for use with Jackson-Labs "Fury" _(not required)_ ##

  * [GPScon](http://www.realhamradio.com/gpscon-info.htm)
  * [Firmware Updater](http://www.jackson-labs.com/assets/uploads/main/flash_isp_utility_lpc2000(1).zip)

## Jackson-Labs "Fury" GPSDO ##

I decided to use a fairly expensive very well known GPSDO made by "Jackson Labs" named "Fury".  I got this one ("only powered up once" by the seller) on Ebay for $380.00 USD plus $15 for shipping.  These run about 2x that direct from the OEM.

[Fury User Manual](https://cdar.googlecode.com/files/Fury_user_manual.pdf)

**note:** This GPS came with v1.18 Firmare installed.  On 4/18/2013 I upgraded it to v1.22

![https://cdar.googlecode.com/files/gpsdo_fury_1.jpg](https://cdar.googlecode.com/files/gpsdo_fury_1.jpg)
![https://cdar.googlecode.com/files/gpsdo_fury_2.jpg](https://cdar.googlecode.com/files/gpsdo_fury_2.jpg)
![https://cdar.googlecode.com/files/gpsdo_fury_3.jpg](https://cdar.googlecode.com/files/gpsdo_fury_3.jpg)
_Desktop Version_
![https://cdar.googlecode.com/files/gpsdo_fury_4.jpg](https://cdar.googlecode.com/files/gpsdo_fury_4.jpg)



## PCTEL - GPS-TMG-26N GPS 26dB Gain Antenna ##

Ant a GPS timing antenna made by "PCTEL" named "**GPS-TMG-26N** GPS 26dB Gain Antenna" this comes with a 50 Ohm N connector built in, as well as an onboard LNA for ["L1" frequencies](http://en.wikipedia.org/wiki/GPS_signals).  It will be mounted at about 10 feet above ground about 25 feet of LMR400 will be used to bring the signal into the GPS.

I purchased this on Ebay for around $60 USD.

[PDF File - Specification](https://cdar.googlecode.com/files/GPS-TMG-26N_Antenna.pdf)

![https://cdar.googlecode.com/files/pctel_antenna_1.jpg](https://cdar.googlecode.com/files/pctel_antenna_1.jpg)
![https://cdar.googlecode.com/files/pctel_antenna_2.jpg](https://cdar.googlecode.com/files/pctel_antenna_2.jpg)