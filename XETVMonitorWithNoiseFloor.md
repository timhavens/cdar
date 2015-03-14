|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

#Monitor XETV (55Mhz) for Backscatter using Yaesu FTDX-5000, and Innovantenna's 10 El. LFA-HZE.

# Introduction #

Using [Spectrumlab](http://www.qsl.net/dl4yhf/spectra1.html) I am able to capture my Yeasu FTDX-5000's 9Mhz IF out via [LP-Pan](http://www.telepostinc.com/LP-PAN.html) to a [E-Mu 1212m](http://www.creative.com/emu/products/product.aspx?category=505&pid=19169) Sound card.  The 192khz IQ is then being plotted using Spectrumlab. It's possible to setup small bandwidth windows that you want to monitor.

Additionally it's possible to use spectrumlabs function 'noise(freq1,freq2)' to define a bandwidth you want to monitor the Noise Floor with.

With a little patience I was able to find where 55.240, 55.250, and 55.260 are in the spectrum being monitored.

Then I setup discrete 'channels' for the "SL Watch List and Plotter" to monitor.

Each channel displays Avg, Max, and Min so you see a nice range for each time moment being plotted per channel.

# Details #

(current version)
![http://cdar.googlecode.com/files/XETV_Es_2013-02-11a.jpg](http://cdar.googlecode.com/files/XETV_Es_2013-02-11a.jpg)
(current version)
![http://cdar.googlecode.com/files/XETV_Es_2013-02-11b.jpg](http://cdar.googlecode.com/files/XETV_Es_2013-02-11b.jpg)

(older version)
![http://cdar.googlecode.com/svn/wiki/Fullscreen%20capture%201192013%2054706%20PM.jpg](http://cdar.googlecode.com/svn/wiki/Fullscreen%20capture%201192013%2054706%20PM.jpg)

and this showing a nice Ms burst.

(older version)
![http://cdar.googlecode.com/svn/wiki/Fullscreen%20capture%201192013%2055640%20PM.jpg](http://cdar.googlecode.com/svn/wiki/Fullscreen%20capture%201192013%2055640%20PM.jpg)