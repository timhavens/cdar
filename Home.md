|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

**50 Mhz RF propagation** using **"Chirp Radar"** and reasonably low-cost hardware and software solutions.

# Introduction #

This project explores various methods, hardware, and software in order to track maximum usable frequency as it approaches and/or exceeds 50 Mhz.  Specifically discovery of propagated paths at 50 Mhz.  The main method being that of "Chirp Radar".

![https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%281%29.jpg](https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%281%29.jpg)

![https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%282%29.jpg](https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%282%29.jpg)

![https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%283%29.jpg](https://cdar.googlecode.com/files/cdar_system_rack_mounted%20%283%29.jpg)

![https://cdar.googlecode.com/files/2013-04-07_work_completed_1.jpg](https://cdar.googlecode.com/files/2013-04-07_work_completed_1.jpg)

![https://cdar.googlecode.com/files/2013-04-07_work_completed_2.jpg](https://cdar.googlecode.com/files/2013-04-07_work_completed_2.jpg)

![https://cdar.googlecode.com/files/pwrbay_sdrbay_pindvr_1kw_switch.jpg](https://cdar.googlecode.com/files/pwrbay_sdrbay_pindvr_1kw_switch.jpg)


# Desired End Result #

## PASSIVE ##

  * In the end we want to study the near 24/7 Meteor Scatter that can be seen on 55.240/250/260 Mhz TV Ch2 out of Canada and Mexico (and other areas in NA) [here](XETVMonitorWithNoiseFloor.md).  Not only is it useful to obtain a baseline running average for Ms on these carriers, but it's also useful to know that baseline and compare it to other types of propagated openings like foEs, and foF2.  NW0W has monitored XETV carriers during EU, SA, JA, and SPAC (ZL/VK) openings for the past 5 years, and has noted some very useful detail related to Backscatter from these carriers.  So we want to make use of this data as long as these 55 Mhz carriers are still on air.

  * We also want to monitor other TV Video such as European, Asian, Eu-Asian and African.  Although one of the main reasons for this project is to be able to realize propagation WITHOUT these carriers, since they seem to be fast disappearing.

## ACTIVE ##

  * **THINKING WHAT'S NEXT!?** (when 45-55 TV carriers are all gone)
> > What are we left with for 'indicators' once 45-55Mhz TV are all gone?
    * 100w CW Beacons (rarely useful at distances of 10,000km+!
    * **Monostatic** Radar (where we can emit "chirps" and obtain things like range, doppler, phase
    * **Bistatic/Multistatic** Radar (similar to monostatic except that it uses a TX 'beacon' and remote "RX Sites") 'bistatic' is one TX and a remote RX, 'multistatic' is one TX and several RX's.  Use of more than one RX site provides even great detail like phase, doppler, azimuth to refraction points.

# Details #

Inspired by VK3OE [Article](http://cdar.googlecode.com/files/BistaticRadar.pdf) ("Bistatic Chirp Radar") and VK6APH ("Hermes/openHPSDR") as well as K5CM and K6QXY (Use of CW "Pings" to detect reflection points at Es and F2).

## Block Diagram ~ Rough Draft ##
(subject to change as project progresses)
![http://cdar.googlecode.com/files/CDAR_FIRST_DRAFT.jpg](http://cdar.googlecode.com/files/CDAR_FIRST_DRAFT.jpg)

  * One of the **MAJOR hurdles** to overcome in 'monostatic' radar is **T/R**switching times in under 1ms (millisecond) as well as RX-settle-Time.
  * **Bistatic** vs. **Monostatic** Radar and related issues.
  * **Chirp** vs. **Ping**
  * **Monostatic Hardware** possibilities:
    * **Transceivers** COTS (commercial off the shelf)
      * Ham Radio's such as (Yaesu, Kenwood, Icom, etc...)
      * Ettus N210 (Xilinx® Spartan® 3A-DSP 3400 FPGA) [here](http://www.ettus.com)
      * openHPSDR "High Performance Software Defined Radio"
        * openHPSDR: [here](http://openhpsdr.org/)
        * Apache-Labs:
          * Hermes (Cyclone 3 FPGA) [here](https://apache-labs.com/al-products/1022/OpenHPSDR-Hermes-Transceiver-Card-Assembled--Tested.html)
          * ANAN-10 (Cyclone 3 FPGA) [here](https://apache-labs.com/al-products/1030/ANAN-10-Transceiver.html)
          * ANAN-100D (Cyclone 4 FPGA) [here](https://apache-labs.com/al-products/1027/ANAN-100D-HF---6M-100W-ALL-MODE-SDR-TRANSCEIVERPREORDER.html)
        * Altera
          * Cyclone III [here](http://www.altera.com/devices/fpga/cyclone3/cy3-index.jsp)
          * Cyclone IV [here](http://www.altera.com/devices/fpga/cyclone-iv/cyiv-index.jsp)
      * PerVices Noctar [video](http://www.youtube.com/watch?v=lzF3dBaz3nE)
        * [PerVices Noctar First Look](http://www.hamradioscience.com/per-vices-noctar-sdr-card-first-look/)
        * [PerVices Noctar Video](http://www.youtube.com/watch?feature=player_embedded&v=6dzqEuCUa1Y#!)
        * [Noctar Y! Group](http://groups.yahoo.com/group/noctar/)
    * **GPSDO**
      * Jackson-Labs "FURY" [here](http://www.jackson-labs.com/index.php/products/fury) **and** [User Manual](http://www.jackson-labs.com/assets/downloads/Fury_user_manual.pdf)
      * Trimble "Thunderbolt" [here](http://www.novotech.com/sites/default/files/Thunderbold-E-GPS-Disciplined-Clock.pdf)
      * Power Supply "Phase Noise" FAQ: [here](http://www.leapsecond.com/pages/tbolt/noise.htm)
    * **High Speed T/R Switching (monostatic)**
      * HIGH POWER (1kw+) TR PIN SWITCH [here](http://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)
      * LOW POWER TR PIN SWITCH
        * These are useful for switching the lo-pwr RF out from the radio away from the PA's very quickly (safety!)
        * Mini-Circuits ZSDR-230+ SPDT Pin Diode Switch [here](http://www.minicircuits.com/pdfs/ZSDR-230+.pdf) SWITCHING TIME 2-4 (μSEC)
        * Mini-Circuits ZFSWHA-1-20 Coaxial High Isolation Switch [here](http://www.minicircuits.com/pdfs/ZFSWHA-1-20+.pdf) SWITCHING TIME 3-10 (ns)
      * 
    * **Antennas**
      * Innovantenna [here](http://www.innovantennas.us)
        * [10L X-POL](http://www.innovantennas.us/index.php?option=com_virtuemart&view=productdetails&virtuemart_product_id=302&virtuemart_category_id=25&Itemid=167) 15.8dBi / 13.65dBd
        * [12L X-POL](http://www.innovantennas.us/index.php?option=com_virtuemart&view=productdetails&virtuemart_product_id=304&virtuemart_category_id=25&Itemid=167) 16.57dBi / 14.42dBd
        * [14L X-POL](http://www.innovantennas.us/index.php?option=com_virtuemart&view=productdetails&virtuemart_product_id=305&virtuemart_category_id=25&Itemid=167) 18.11dBi / 15.96dBd
    * **Software**
      * GNURadio [here](http://gnuradio.org/redmine/projects/gnuradio/wiki)
      * **cuSDR** [here](http://svn.tapr.org/repos_sdr_hpsdr/trunk/DL3HVH/cuSDR64/)
      * CUDA [here](http://www.nvidia.com/object/cuda_home_new.html) **and** [here](http://www.nvidia.com/content/cuda/spotlights/brian-fanous-mathworks.html)

# TEST RESULTS VIDEO'S #

<a href='http://www.youtube.com/watch?feature=player_embedded&v=4aJf9nT58PM' target='_blank'><img src='http://img.youtube.com/vi/4aJf9nT58PM/0.jpg' width='425' height=344 /></a>