#This is NW0W's version 2 RTL SDR for 9Mhz IF

# Introduction #

This is my most recent version of an RTL SDR for my FTDX-5000 for use with the 9Mhz IF Out.

  * This box uses
    * NooElec R820T RTL
    * NooElec HamItUp 125Mhz Upconverter (uses a modified power cable direct to the MeanWell 5v supply)
    * MeanWell 120vac/5vdc PS
    * CorCom EMI Filter (120vac)
    * SIIG SS-USB3.0 Powered Hub powered from MeanWell PS
    * LNA-3000a
    * VHF-FM Stop-Band FM-Band Notch Filter
    * Two Ferrite Torriods
    * Packed into a Hammond Case
    * Double Sided Copper PCB's to create shelves, and compartments
      * in order to reduce RFI/EMI between components

  * This has resulted in a better than expected >95% reduction in 'birdies' and odd spurs, etc.

  * While the LNA is NOT a requirement, it certainly aids in NOT having to use any of the RTL Gain or very low amounts.  I generally have been using 1db of RTL Gain, and RTL AGC = ON.

# Details #

![https://cdar.googlecode.com/files/rtl_sdr_if_panadapter%20%288%29.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_panadapter%20%288%29.jpg)

![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_1.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_1.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_2.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_2.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_3.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_3.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_4.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_4.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_5.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_5.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_6.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_6.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_7.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_7.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_8.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_8.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_9.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_9.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_10.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_10.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_11.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_11.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_12.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_12.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_13.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_13.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_14.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_14.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_15.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_15.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_16.jpg](https://cdar.googlecode.com/files/rtl_sdr_upconverter_v2_16.jpg)

# IF-INHIBIT Switch #

## WHY THIS? ##

  * I don't want the 9Mhz Out impacting CWSKIMMER by my own CW Transmissions.
  * This uses a simple 12v supply and GND line to 'flip-flop' the SMA relay.
  * I've built another one that uses a micro-switch-reed-relay and 26v, but I have yet to try and integrate this into my sequencer system.

![https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_1.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_1.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_2.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_2.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_3.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_3.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_4.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_4.jpg)
![https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_5.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_inhibit_switch_5.jpg)