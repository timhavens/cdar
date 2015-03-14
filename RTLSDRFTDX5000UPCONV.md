#RTL-SDR AND "Hamitup" (converter) USB used as an SDR to HDSDR for FTDX-5000

# RTL SDR IF Pan-Adapter #

![https://cdar.googlecode.com/files/dont_interrupt.jpg](https://cdar.googlecode.com/files/dont_interrupt.jpg)

![https://cdar.googlecode.com/files/rtl_sdr_if_panadapter%20%288%29.jpg](https://cdar.googlecode.com/files/rtl_sdr_if_panadapter%20%288%29.jpg)
[RTL SDR IF PANADAPTER HERE](https://code.google.com/p/cdar/wiki/NW0WRTLSDR)

**[How I 'boxed' my upconverter](https://plus.google.com/u/0/photos/109081672217576088028/albums/5896065518073329073)**


[Excellent Documentation on the Upconverter](https://code.google.com/p/opendous/wiki/Upconverter)
**So NooElec's documentation indicates about 10db loss over the upconversion.  I am using a 17.5db gain LNA (very wide lna)**

[Here is an FB LNA for next to nothing](http://lna4all.blogspot.com/2013/04/lna-for-all-low-noise-amplifier-for.html)

Your experience may vary, but you might want to consider using an LNA as well.  That's up to you and your particular setup.

![https://cdar.googlecode.com/files/rtl_to_ftdx_block_2.jpg](https://cdar.googlecode.com/files/rtl_to_ftdx_block_2.jpg)

# Introduction #

Today I received my "HamItUp" (upconverter) which takes HF signals and upconverts them to whatever the frequency was at HF + 125Mhz.  For example my FTDX-5000 has a 9Mhz IF Output.  I've connected the upconverter to my 9Mhz output, and set HDSDR to use the RTL dongle at an IF of 134Mhz.

Immediately I noticed that **I had more 'birdies' using this method**, and actually I expected fewer.  So...after a bit I had the idea of using a toroid on the USB Power cable which powers the upconverter from the PC.  I used 7 wraps of the cable around a doughnut shaped toroid and WAH-LAH the birdies are gone.  Ok, I was amazed by that.  Maybe I shouldn't be, but the fact remains :-) [these are the ones I used](http://www.newark.com/fair-rite/5943003801/ferrite-core-toroid-43/dp/27C1651?Ntt=5943003801) but likely any would work.  I used one on each end of the usb cable.  You need a long enough cable to get about 7 turns on it.  Other options are to use a battery-extender for a cellphone where the battery would act as a filter and it can be plugged into the wall charging while you use it, and or a usb cable that has ferrites on both ends.

Okay so...this isn't that different from the 'Tee' method I've previously described [here](https://code.google.com/p/cdar/wiki/RTLSDRFTDX5000).  **If you haven't read this yet, you might want to.**

The exception to this previous method is that this method using the 9Mhz IF output on the FTDX-5000 (it could just as well use any HF IF frequency as well).  All that's required is to know the HF IF frequency, and add 125Mhz to it, and HDSDR will be very very close.  Should be within 1-2Khz.  This can be corrected as well to the point where you are within just a few hertz on your HDSDR display.

The cheapest source to find an R820T chipset USB TV Dongle it Ebay.  I've bought several from there specifically from a user there named "Chinarf".  However, if speed is your game you can purchase the same thing from [Nooelec.com here](http://www.nooelec.com/store/software-defined-radio/sdr-receivers/tv28tv2.html#.UciqBvnviqc)

The "HamItUp" converter can be purchased  [Upconverter sold here](http://www.nooelec.com/store/software-defined-radio/sdr-accessories/ham-it-up-v1-0-rf-upconverter-for-software-defined-radio.html#.Uccf8vnviqc)

**BEWARE there IS a short warm-up time for the 125Mhz xtal to stabilize**

I've seen the Upconverter take about 3-5 Minutes to stop drifting.  Cold it starts about 200-300hz high and slowly drifts down to where it was previously calibrated to.  Just don't freak out if you see this happen when you first turn it on.

What I've done today is to use a $15 USB TV RTL 'dongle' with a chipset of R820T and a $43 upconverter as a direct replacement for nearly $600 worth of equipment WITH FAR BETTER RESULTS!  In short "It's STUNNING".

**This isn't an all inclusive manual.**  It's a starting point.  You may need to alter some of the configurations to suit your taste and or requirements.

This setup is very simple but has many steps.

If you are already a user of HPSDR then this won't be all that foreign to you.  In fact I think it's actually simpler to setup than using one of the sound-card / LP-Pan setups (which I've been using for years).

## Brief Parts List ##
From the 9Mhz IF out on the back of my FTDX-5000 there is a Female RCA conn:

  * RCA(M) to BNC(F) adapter
  * BNC(M) to SMA(M) 12" RG400 Jumper
  * SMA(F) conn (INPUT) port on "HamItUp" 125 Mhz Upconverter
    * There is a USB-B (printer port type conn) that is connected to my PC after loops through a torroid.
      * This powers the Upconverter.
  * SMA(F) conn (OUPUT) port on "HamItUp" 125 Mhz Upconverter to 12"  SMA(M) / SMA(M) jumper
    * This jumper connected to IN of a Par 'VHF-FM' Broadcast band-stop filter: [here](http://www.parelectronics.com/fm-broadcast.php) (Just for grins)
  * Output of the VHF-FM connected to 'IN' LNA-3000B 17.5db (1.3db NF) LNA
    * http://rfbayinc.com/product_info.php?cPath=1_83&products_id=111
    * http://rfbayinc.com/products_pdf/product_111.pdf
    * Recommended LNA: [HERE](http://lna4all.blogspot.com/2013/04/lna-for-all-low-noise-amplifier-for.html) **WAY Cheaper**
  * Short Jumper from LNA OUTPUT SMA(M) to MCX(m) which plugs into the RTL
  * This RTL is similar to the one I have: http://www.nooelec.com/store/software-defined-radio/sdr-receivers/tv28tv2.html#.UdK7ZvnviuI

So there's a small power supply for the LNA I'm using also not already mentioned.

Now here is the deal, there is about 10-15db loss in the 125Mhz upconversion so to compensate I added the LNA.
I haven't removed it since I added it to test without it because things are just about perfect for my taste.  **N2TU** is running his setup similar to mine minus the VHF-FM and LNA with very good results.  This just requires a bit more gain in the RTL setup than I'm using.

## Hardware Setup: ##

You will be using your radio's Lo-Band 'IF OUT'.  Hopefully your radio already has an IF OUTPUT, if not you should start looking at mods for your specific radio or it's schematic in order to resolve how best to tap the IF.  If you radio has an IF OUT already, and it's not say 6-9Mhz but instead > 50Mhz, you could just directly connect the R820T to that VHF IF Output and you should just about be done + some software configuration.

To use the IF-OUT on the FTDX-5000 you need to get to menu item #109 and set it to 'enable'.

![https://cdar.googlecode.com/files/hamitup_upconverter.jpg](https://cdar.googlecode.com/files/hamitup_upconverter.jpg)

  * Connect the HamItUp upconverter's INPUT port to your IF-OUT on the radio.
  * Connect the HamItUp OUPUT to your RTL MCX antenna connector.
  * Connect the HamItUp USB power cable to an available usb port.
  * Flip the switch labeled 'ByPass' to 'upconvert' (switched towards the RF output connector).

![https://cdar.googlecode.com/files/hamitup_power_cable_and_toriod.jpg](https://cdar.googlecode.com/files/hamitup_power_cable_and_toriod.jpg)
**(with toriod added!!!!)**

![https://cdar.googlecode.com/files/LNA.jpg](https://cdar.googlecode.com/files/LNA.jpg)
**LNA** http://www.rfbayinc.com/upload/files/lna/lna-3000b.pdf (pretty sure you **don't need this!**)

![https://cdar.googlecode.com/files/R820T_with_msx_to_sma.jpg](https://cdar.googlecode.com/files/R820T_with_msx_to_sma.jpg)
**(R820T)**

**THAT'S IT** for the basic connection between the FTDX-5000 and your RTL dongle.

If your RTL doesn't seem to show signals on your display you may require a small 10-15db preamp between the upconverter and the RTL dongle.  I use a 19db LNA here.  But it's probably not required.  The dongle has a fair amount of gain built in.  This should cover whatever the upconverted frequency is when it leaves the HamItUp output.  In my case 134Mhz with the FTDX-5000.  The LNA I'm using is VERY wide banded, and doesn't have a very nice NF something like 1.3db.  BUT it works just fine.  Since all I'm trying to do is SEE RF signals that my EAR is able to hear in my radio which isn't affected by this LNA's NF.  But you do whatever you have to and are happy with.

# (Shameless 4sale Ad) #

I have in excellent condition an LP-Pan with the K3 preamp mod installed, some cabling, and an Emu-1212M sound card combo.

Those interested should email me here:

![https://cdar.googlecode.com/files/email.jpg](https://cdar.googlecode.com/files/email.jpg)

# Videos #

I'm currently waiting for some decent openings to show this setups potential.  I'll also get some video of very weak openings so that you'll see how the system functions with weak signals as well.

## HamItUp Method ##
<a href='http://www.youtube.com/watch?feature=player_embedded&v=P0ptFsM83Qo' target='_blank'><img src='http://img.youtube.com/vi/P0ptFsM83Qo/0.jpg' width='425' height=344 /></a>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=_Noln8pVKp0' target='_blank'><img src='http://img.youtube.com/vi/_Noln8pVKp0/0.jpg' width='425' height=344 /></a>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=RgDH2904c9A' target='_blank'><img src='http://img.youtube.com/vi/RgDH2904c9A/0.jpg' width='425' height=344 /></a>


---


Install your R820T chipset RTL USB "dongle" in a USB2.0 or faster port

Connect a MCX to SMA (or BNC) jumper to your RTL Dongle. MCX end goes to the dongle, the other end goes to either your Tee or your Preamp hanging off the Tee.

You will also want to have a serial port available to control your FTDX-5000.  This way when you click on a signal in the HDSDR program, your radio will QSY there and inversely if you tune the radio the HDSDR will sync with your radio's VFO.

## Software Setup: ##

[Howto Test the max sample-rate your PC and RTL can handle without data loss](https://code.google.com/p/cdar/wiki/RTLSDRTEST)

Download the following three bits of software:
  * Zadig: http://sourceforge.net/projects/libwdi/files/zadig/ (get the most recent version)
    * http://rtlsdr.org/softwarewindows (details on how to use zadig are here)
  * HDSDR: http://www.hdsdr.de/
  * ExtIO\_RTL: https://github.com/josemariaaraujo/ExtIO_RTL/blob/master/Release/ExtIO_RTL.dll

Install HDSDR (just install it at this point more to come on this later)

Place the ExtIO-RTL.dll in the directory where you just installed HDSDR.

Now run HDSDR by clicking on HPSDR.exe

Click 'Options' > 'Cat to Radio (omni-rig)' > 'Omni-Rig Setup'
You should already have CAT enabled on your FTDX-5000 and know how it's setup there in order to configure this area.  This is what it looks like for mine.

![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%285%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%285%29.jpg)

Click 'Options' > 'Cat to Radio (omni-rig) ensure these options are set.
![https://cdar.googlecode.com/files/rtl_sdr_cat_to_hdsdr.jpg](https://cdar.googlecode.com/files/rtl_sdr_cat_to_hdsdr.jpg)

  * Click on ExtIO you should see something like this (be sure to test out larger buffer sizes to see if your computer handles them I'm currently using 8kb rather than the 2kb the images shows) :
![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%286%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%286%29.jpg)
  * Initially configure yours to appear like this image shows.
  * click on the 'x' and exit that screen.

Now click on "Options" (lower left of HDSDR) > "Select Input" and just verify that "RealTek" is checked See image below.

![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%2810%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%2810%29.jpg)

Now click on soundcard, and configure your sound card.

![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%288%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%288%29.jpg)

Click on 'OK'.

Now Click on 'Bandwidth' This brings up a small window with two columns on the right side if the sound card output sample-rate you can set this to anything that works best for your ears and your sound card.  I've used 12000 up to 96000 and my ears barely pick up a change.  I have a fast computer with cycles to spare on the CPU and a good sound card, so I'm currently using 96000.  But as I said they all seemed to work about the same to my ears, however your experience may vary, so you may want to revisit this area and try several of them once you get things running.

![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%289%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%289%29.jpg)

Now click on 'Options' > 'Visualizations' > 'RF Spectrum Type'.
There are two options here 'Amplitude Spectrum' and 'Power Spectral Density' The default is 'Amplitude Spectrum'.  That's what I'm currently using but I've tried both in varying conditions, and depending on how the band is at the moment one may display better than the other.

![https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%2811%29.jpg](https://cdar.googlecode.com/files/rtl_sdt_ft5k%20%2811%29.jpg)

Now click on 'Options' > 'Visualizations' > 'FFT Windowing' I'm sure this are will bring a fair amount of debate for those who are experienced SDR users.  The short story is that I choose to use 'Hamming' or 'Blackman' here.  TRY them and see which of the available options works best for you once you have things running.

Now click on 'Options' > 'Visualizations' once again (yes clicking on options is a pain in the butt when you have to set all these items up one at a time like this).

In the image above make sure you have the items that are selected at this level 'selected/checked'.

Click 'Options' > 'Input Channel Mode for RX'
Select 'I (Left)/Q (Right)'

Click 'Options' > 'Output Channel Mode for RX'
Select 'AF to Both Channels'

Click 'Options' > 'Input Channel Calibration for RX'
Make sure that 'Mode' is set to 'Auto' and click 'OK'
And 'Hz' = 1 (you can mess with this later if you have to)

Click 'Options' > 'Misc Options'
Select 'Tune Fixed to LO'
If you have a fast computer also select 'High Process Priority'

Click 'Options' and ensure that 'Swap I and Q channel for RX input' **IS** selected.  **This is different from the 'Tee' Method!**

Click 'Options' > 'RF Front-End + Calibration'
(This area is simple yet complicated if you don't understand what's going on) at this point you'll need some accurate signal source on 28Mhz or 50Mhz.  I used a small XG3 from Elecraft seen in one of the photo's above.  This generates a signal on 50.097 Mhz so that I was able to quickly get through this section.
  * First select 'SDR on IF output, which is controlled - **by Omni-Rig**'
  * Set Sync Mode = 'Full sync in both directions'
  * Set IF-Frequency = 134000000 Hz
  * Set Global Offset = 293 Hz (you made need to tweak this some)
  * Set LSB = 1500
  * Set USB = -1500
  * Set CW\_U = -600
  * Set CW\_L = 600
  * Click 'OK'
  * Click HDSDR 'START' button.  You should see the waterfall functional at this point.
  * Locate your signal source on the display, it shouldn't be too far off.  If you have to zoom in/out to get within 20Khz do that, this might help you find the carrier.

Now we need to mux around with Global Offset here Click 'Options' > 'RF Front-End + Calibration'.
  * Once you've located the carrier you will need to enter the 'Global Offset in [Hz](Hz.md) and click the 'OK' button in order to view the results of the change.

You may have to do this quite a few times.  If you see the carrier on your screen moving in the right direction continue by entering a new 'Global Offset' until you get the carrier to display exactly on frequency.  BETWEEN each attempt you will want to click 'OK' before you enter a new 'Global Offset' and then 'OK'.  Once you are on the carrier and it shows up on you screen to your satisfaction click on 'OK'.

**THIS IS NEW TO ME TOO**  This is just a basic setup process I used to make this work with HamItUp upconverter by NooElec.com.  If you have any bugs, questions, or comments please email them to me at the email address noted above!

## CWSKIMMER Using HDSDR As SDR ##
https://code.google.com/p/cdar/wiki/HDSDRCWSKIMMER

# HELP #
  * https://sites.google.com/site/g4zfqradio/installing-and-using-hdsdr
  * http://www.hdsdr.de/faq.html

## Misc ##
http://research.physics.illinois.edu/bezryadin/labprotocol/SIF-50.pdf


---

[Other Ham Similar setups and contributions](https://code.google.com/p/cdar/wiki/RTLSDRUSERS)

---
