|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

Pin Switch Driver (example)

# Details #
  * **Important Note**: WE NEED TWO of this circuit.  One Per Diode on the HP TR Switch. (D1, D2)
  * 2A +/- 15vdc (dual output) Supply min. [HP 62215E will be used](https://code.google.com/p/cdar/wiki/HP_62215E) and provides up to 3A! (cheap on Ebay!)
  * VK3OE designed a nice, simple Pin Driver that even includes a TX-Inhibit Line which can be used to check that the HP Switches **are switched**

![https://cdar.googlecode.com/files/PIN_DRIVER_v2.6.jpg](https://cdar.googlecode.com/files/PIN_DRIVER_v2.6.jpg)

# NW0W Prototype #

![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_3.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_3.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_2.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_2.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_1.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_1.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_4.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_4.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_5.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_5.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_6.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_6.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_7.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_7.jpg)
![https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_8.jpg](https://cdar.googlecode.com/files/vk3oe_15vdc_ping_driver_8.jpg)

![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2811%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2811%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2812%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2812%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2813%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2813%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2814%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2814%29.jpg)
## transmit fault ##
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2815%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2815%29.jpg)
## transmit ok ##
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2816%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2816%29.jpg)
## receive ok ##
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2817%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%2817%29.jpg)

# NOTES #

  * So I just finished testing voltages.
  * So things look pretty close I think.
    * J1 (ON) "transmit"
      * J3 (TX) = +0.08 "OK"
    * J1 (OFF) "receive"
      * J3 (RX) = -0.000
    * Fault = +0.48 to 0.5v (like disconnecting line to the PIN diode, on TX)
    * PIN Voltages on TX = +1.011v (D1), +0.930v (D2)