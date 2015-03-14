|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

#50 Mhz 1kw+ Low Pass Filter ~ K1WHS Design

# Introduction #

Normally I'd just slap an ICE 427 LPF on the end of a 50Mhz PA and be done.  However ICE no longer appears to be making these anymore.  K1WHS has a very simple design that should work just fine.

# Details #

![http://cdar.googlecode.com/files/50Mhz_LPF_K1WHS.jpg](http://cdar.googlecode.com/files/50Mhz_LPF_K1WHS.jpg)

# TODO #

  * Attach 4-screw N-connectors (current ones SUCK shown in photo's)
  * Replace screws with SS (photo's show temp screws for mock up)

# COMPLETED #

  * Re-position Caps to allow for Term. Lugs (photo's show they're too close as of 3/16 - completed 3/17)
  * Test Low-Power
  * Test 1.5Kw

# Images #

![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_1.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_1.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_2.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_2.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_3.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_3.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_4.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_4.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_5.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_5.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_6.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_6.jpg)
![https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_7.jpg](https://cdar.googlecode.com/files/K1WHS_50Mhz_LPF_7.jpg)

## PARTS LIST ##

|50pf 15kvdc 1.187" diameter, 1.89" long, 10-32 UNF thread.|SurplusSales|(CFC) HT570050-15|(CFC) HT570050-15|HEC|$42.00|2|$84.00|[here](http://www.surplussales.com/capacitors/Trans_Coup_Caps/cap_doorknob.html)|
|:---------------------------------------------------------|:-----------|:----------------|:----------------|:--|:-----|:|:-----|:-------------------------------------------------------------------------------|
|12 AWG Magnet Wire|Ebay|12 AWG|- |Temco|$6.10|1 |$6.10|[here](http://www.ebay.com/itm/Magnet-Wire-12-AWG-Gauge-Enameled-Copper-4oz-12-5ft-200C-Magnetic-Coil-Winding-/251059969039?pt=LH_DefaultDomain_0&hash=item3a74571c0f)|
|N-Type Connector Bulkhead|Ebay|- |- |- |$3.29|2 |$6.58|[here](http://cgi.ebay.com/ws/eBayISAPI.dll?ViewItem&item=370658907688&ssPageName=ADME:L:OU:US:3160)|
|Alum Case 7.38"x4.7"x3.07"|Mouser|546-1590EF|1590EF|Hammond|$32.99|1 |$32.99|[here](http://www.mouser.com/ProductDetail/Hammond-Manufacturing/1590EF/?qs=sGAEpiMZZMsrGrAVj6eTvYHXIhi3B2FeyZoATIcNtTE%3d0)|
|**TOTAL**|  |  |  |  |  |  |$129.67|- |