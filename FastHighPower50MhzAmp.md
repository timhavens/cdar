|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

SSHP 50Mhz Amp with VERY FAST T/R Switching (for pulsing)

# Status #

  * 2013-04-19 Most of the other equipment is now purchased, and built.  The Amp is the last of the big dollar items (although the price is very reasonable)!  I intend to order and build/install the amp the first weeks in May.

# Details #

The amp we're going to use is a 900w (capable) with 2.2w INPUT, likely running only about 200-300w for this project normally.  [From Broadcast Concepts](http://www.broadcastconcepts.com/FM-Amplifiers-30w-2kW/FM-Pallet-Amplifiers/BLF178XR%20900W%20FM%20Pallet%20Amplifier).  Mounted on a [13.5" Heatsink](http://www.broadcastconcepts.com/Pallet-Amp-HeatSinks/13.5%22%20Bonded%20Heat%20Sink).

I already have an [amp control board](http://www.w6pql.com/amplifier_control_board.htm) as well as a [Dual RF Sampler](http://www.w6pql.com/Sampling_RF_Power.htm) for amp protection.

This will be mounted in a 19" x 10" Hammond Rack Mountable Enclosure.

The PA Power Supply is small enough to fit in the "PowerBay" we already have, and installation of other system related PS's was done in order to accomodate [this](http://www.broadcastconcepts.com/DC-Power-Supplies-Pallet-Amps/MeanWell%201500W%2048V%20DC%20Power%20Supply) 50v @ 32A supply.

Apache-Labs "Hermes" power output appears to be around 380-400mW.  This should be adequate to drive this PA up to about 200+ Watts, which is on target with what we wanted to start with.

At some point in the future we may add a small 'booster' amp to be able to drive the PA up to full rated (safe) power out.

## Related Items ##

  * **Low Pass Filter**
    * [50Mhz LPF](http://code.google.com/p/cdar/wiki/50Mhz_1kw_Low_Pass_Filter_K1WHS)

  * **T/R Switches**
    * [50Mhz 1kw Pin Switch](http://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)

## Some External Links of Interest ##

  * [Booster Amp 400mw pIN / 15W pOUT](http://www.broadcastconcepts.com/FM-Amplifiers-30w-2kW/FM-Pallet-Amplifiers/FM-Pallet-Drivers?product_id=158) (would require some tuning down)
  * [Booster Amp 0dbm (1mw) pIN / 12W pOUT](http://www.broadcastconcepts.com/TV-Amplifier/TV-Amplifiers-55-88MHz%20-LO-VHF/55-88MHz%2012W%20Band%20I%20VHF%20TV%20Driver) (would require 26dbm pad)
  * [BC -  Pallet Amps](http://www.broadcastconcepts.com)
  * [BC - RF Overdrive Board](http://www.broadcastconcepts.com/coax-heatsinks-power-supplies-resistors-fans-/RF%20Overdrive%20PCB%2030%20to%20250MHz)
  * [BC - Amp Power Supply](http://www.broadcastconcepts.com/DC-Power-Supplies-Pallet-Amps/MeanWell%201500W%2048V%20DC%20Power%20Supply)
  * [W6PQL](http://www.w6pql.com/)
  * [W6PQL - Amp control board](http://www.w6pql.com/amplifier_control_board.htm)
  * [Winford Eng](http://www.winfordeng.com/products/cat_brk.php)
  * [NXP BLF578](http://www.nxp.com/documents/data_sheet/BLF578.pdf)
  * [BLF178XR](http://www.broadcastconcepts.com/FM-Amplifiers-30w-2kW/FM-Pallet-Amplifiers/BLF178XR%20900W%20FM%20Pallet%20Amplifier)

  * **Tables**
  * ![http://cdar.googlecode.com/files/dbm_to_watts_conv.jpg](http://cdar.googlecode.com/files/dbm_to_watts_conv.jpg)

  * **Misc**
  * [Liquid cooling](http://www.shop.customthermoelectric.com/Water-Block-Assembly-All-Copper-30-x-30-x-085-WBA-30-085-CU-01.htm)