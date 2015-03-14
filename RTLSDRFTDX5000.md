#RTL-SDR USB used as an SDR to HDSDR for FTDX-5000

# Introduction #

Today I decided to try something new.  This took a total of about 45 minutes from start to finish, with no outside directions on how to do it.  SO it's not that difficult.

I operate nearly 100% on 50Mhz.  My radio is a Yaesu FTDX-5000.  For a few years I've been using something called LP-PAN to provide a decent pan-adapter for my radio.  This has worked fine for a few years, but there are some tech issues with this setup.  Most are known short-comings of using a sound-card to pass I/Q to your computer.  I won't go into those details at this point (maybe some other time).

What I've done today is to use a $15 USB TV RTL 'dongle' with a chipset of R820T as a direct replacement for nearly $600 worth of equipment WITH FAR BETTER RESULTS!  In short "It's STUNNING".

I'll outline how I set this up, along with some images to help you orient yourself, and in the end provide details on another option I'm working on as well.

**This isn't an all inclusive manual.**  It's a starting point.  You may need to alter some of the configurations to suit your taste and or requirements.

This setup is very simple but has many steps.

If you are already a user of HPSDR then this won't be all that foreign to you.  In fact I think it's actually simpler to setup than using one of the sound-card / LP-Pan setups (which I've been using for years).

You will be using the ports between RX-IN and RX-OUT.

This also means you'll want to turn on your RX in/out switch on the FTDX-5000.

This method on the FTDX-5000 radio should cover 24Mhz to 60Mhz.  Since 24Mhz is the lowest the RTL dongle covers.

There is another option rather than using RX-in/out you could use your IF OUT if your radio has this.  In this case you need to know the frequency of your IF OUT.  On my FTDX-5000 this is about 9Mhz.  Since the RTL dongles don't cover 9Mhz (>= 24Mhz only) you can purchase from http://nooelec.com something called a 'Ham it UP converter' for about $43.  This upconverts from HF to 125Mhz.  The setup for this is very different than what I'm describing here.  This is covered [here](https://code.google.com/p/cdar/wiki/RTLSDRFTDX5000UPCONV)

I have a short jumper between RX-OUT and a PR6 preamp, and RX-IN.  You won't need the preamp I don't think.  I use this for receive on 6m.  But it is added gain that both the RTL dongle, and the Rcvr will see if you set yours up like this.

If your RTL doesn't seem to show signals on your display you may require a small 10-15db preamp to run off the RTL line of the Tee in your RX-in/out loop.  This way you aren't adding gain to your actual receiver (if you're one of those who don't believe in such things).

# (Shameless 4sale Ad) #

I have in excellent condition an LP-Pan with the K3 preamp mod installed, some cabling, and an Emu-1212M sound card combo.

Those interested should email me here:

![https://cdar.googlecode.com/files/email.jpg](https://cdar.googlecode.com/files/email.jpg)

# Videos #

I'm currently waiting for some decent openings to show this setups potential.  I'll also get some video of very weak openings so that you'll see how the system functions with weak signals as well.

<a href='http://www.youtube.com/watch?feature=player_embedded&v=Q5aC9r6vWHQ' target='_blank'><img src='http://img.youtube.com/vi/Q5aC9r6vWHQ/0.jpg' width='425' height=344 /></a>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=1NzQLU2CZ2c' target='_blank'><img src='http://img.youtube.com/vi/1NzQLU2CZ2c/0.jpg' width='425' height=344 /></a>

# Details #

## Hardware Setup: ##

RX-in/out Loop image HERE
![https://cdar.googlecode.com/files/20130620_172429%20%281%29.jpg](https://cdar.googlecode.com/files/20130620_172429%20%281%29.jpg)

Tee Image HERE
![https://cdar.googlecode.com/files/20130620_172504.jpg](https://cdar.googlecode.com/files/20130620_172504.jpg)

RTL line image HERE

RTL Dongle image HERE
![https://cdar.googlecode.com/files/20130620_172522.jpg](https://cdar.googlecode.com/files/20130620_172522.jpg)


---


Install your R820T chipset RTL USB "dongle" in a USB2.0 or faster port

Connect a MCX to SMA (or BNC) jumper to your RTL Dongle. MCX end goes to the dongle, the other end goes to either your Tee or your Preamp hanging off the Tee.

You will also want to have a serial port available to control your FTDX-5000.  This way when you click on a signal in the HDSDR program, your radio will QSY there and inversely if you tune the radio the HDSDR will sync with your radio's VFO.

## Software Setup: ##

Download the following two bits of software:
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

  * Click on ExtIO you should see something like this:
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

Click 'Options' > 'Misc Options'
Select 'Tune Fixed to LO'
If you have a fast computer also select 'High Process Priority'

Click 'Options' and ensure that 'Swap I and Q channel for RX input' is NOT selected.  (if it is selected LSB will be swapped with USB)

Click 'Options' > 'RF Front-End + Calibration'
(This area is simple yet complicated if you don't understand what's going on) at this point you'll need some accurate signal source on 28Mhz or 50Mhz.  I used a small XG3 from Elecraft seen in one of the photo's above.  This generates a signal on 50.097 Mhz so that I was able to quickly get through this section.
  * First select 'SDR hardware connected to antenna (default)'
  * On the right side of this window is 'LO frequency calibration'
    * Click 'Start' on the main window and you should see the display functioning at this point.
  * Locate your signal source on the display, it shouldn't be too far off.  If you have to zoom in/out to get within 200Khz do that, this might help you find the carrier.
  * Once you've located the carrier you will need to enter the 'correct Tune Frequency [Hz](Hz.md) and click 'Calculate' this will set a Frequency Correction in ppm (parts per million).  You may have to do this quite a few times.  If you see the carrier on your screen moving in the right direction continue by entering a new 'Correct Tune Frequency' until you get the carrier to display exactly on frequency.  BETWEEN each attempt you will want to click 'Reset' before you enter a new 'Correct Tune Frequency' and then 'Calculate'.  Once you are on the carrier and it shows up on you screen to your satisfaction click on 'OK'.

# HELP #
  * https://sites.google.com/site/g4zfqradio/installing-and-using-hdsdr
  * http://www.hdsdr.de/faq.html

## Misc ##
http://research.physics.illinois.edu/bezryadin/labprotocol/SIF-50.pdf