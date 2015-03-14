|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

#In the USA we have to follow the **FCC** rules in part 97.

# Introduction #

  * We need to stay within the [FCC Part 97 Rules.](http://www.arrl.org/files/file/Regulatory/Part%2097%20-%2004-28-2011.pdf)
  * We need to stay within the [ARRL Establish Band-Plan.](http://www.arrl.org/band-plan)

# Details #

> ### FCC Part 97.203, "CDAR" is NOT a beacon! ###
    * "CDAR" will be 'attended operation' ONLY.
    * "CDAR" will operate above 100w.
    * "CDAR" will operate between 50.6 - 50.8 Mhz (nonvoice communications - see ARRL band plan)
```
* "CDAR" will periodically CQ DE <CALLSIGN> QSX <FREQ> 

  * Similar to those calling "VVV CQ <CALL>"

    * The exception is that we will

      * "Chirp" 1 second (500hz-2500hz sweep over 1 second period)

      * listen 1 second (record echos)

      * repeat above for a time

      * Periodically ID every few minutes with the preamble
        * CQ DE <CALLSIGN> QSX <FREQ>
        * ANSWER CALLERS @ QSX <FREQ>
          * While answering callers at QSX <FREQ> all other operations will cease. 
            (only TX one carrier in-band at a time!)

      * LOG Echo Results - Automatically & Publish the results.

      * LOG QSOs - Automatically & Publish the results.
```


> ### ARRL 6m (50 Mhz) Band Plan ###
    * For this type of operation we want to operate well outside the most commonly used freq-ranges to mitigate any interference.
    * Possible Ranges of operation appear to be
      * 50.3 - 50.6 Mhz "All modes" (but commonly AM)
      * **50.6 - 50.8 Mhz** "Nonvoice communication" 