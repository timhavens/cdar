|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

I bought 6 of these MINI-CIRCUITS ZSDR-230 switches on Ebay for $80US.
They are 5vdc, and use TTL to drive the switch between COM and RF1/RF2.
In testing with Hermes this evening I discovered @ 50Mhz it's quite excellent!

There low-power TTL pins switch in about 2ns.  And will be used as a safety protection for both TX and RX ports, to save Hermes from any high power RF that may leak back towards it from the High Power pin switch.  Also as a fail-safe in case anything down the line fails.

As an added safety, we'll be using the Array Solutions AS-RXFEP shown below, on the RX line input from the High Power TR to the low Power TR Safety switch.  It will be the first item on the RX line from the High Power TR RX line, the lower power TR safety will be next, then the LNA and then Hermes RX port.  These sell for about $55 each.

![https://cdar.googlecode.com/files/array_solutions_as-rxfep_1.jpg](https://cdar.googlecode.com/files/array_solutions_as-rxfep_1.jpg)
![https://cdar.googlecode.com/files/array_solutions_as-rxfep_2.jpg](https://cdar.googlecode.com/files/array_solutions_as-rxfep_2.jpg)

# Details #

  * These switches can only handle MAX 100mW (20dbm) @ 50Mhz **SO BE CAREFUL!**
  * At -33dbm injected on COM (not calibrated, Elecraft XG3 used) I saw -37.6dbm at RF2.
  * At -33dbm injected on RF1 I saw -102.5dbm on RF2 at all times.
  * -102.5dbm - -37.6dbm = **-64.9dbm isolation** between RF1 & RF2.
  * XG3 isn't really calibrated at this point and the batteries during test may have been low explaining the -33dbm setting being seen at Hermes @ -37.6dbm.  (more testing will be done to confirm this)
  * Hermes and my PwrSDR app haven't been put through any calibration yet either.  However, I believe the values seen in the test are still valuable enough to show that we have good isolation.
  * This weekend I'll be ordering the J16 26-pin header breakout board.  This will be used to connect various things like PTT, and work on a TX-INHIBIT function from the Pin Driver board.

![https://cdar.googlecode.com/files/ZSDR-230_1.jpg](https://cdar.googlecode.com/files/ZSDR-230_1.jpg)
![https://cdar.googlecode.com/files/ZSDR-230_2.jpg](https://cdar.googlecode.com/files/ZSDR-230_2.jpg)
![https://cdar.googlecode.com/files/ZSDR_230_3.jpg](https://cdar.googlecode.com/files/ZSDR_230_3.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_1.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_1.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_2.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_2.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_3.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_3.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_4.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_4.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_5.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_5.jpg)
![https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_6.jpg](https://cdar.googlecode.com/files/ZSDR-230%20Power%20And%20signal%20Setup_6.jpg)