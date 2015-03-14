#Meteor Detection using inexpensive RTL TV Dongles

# Introduction #

For a few years now I've been using these cheap RTL (R820T, FC0013) TV dongles (about $15-20USD) as inexpensive SDR receivers.  I've been wanting to get one of them working as a Meteor Detector (and counter) for a while now.  This is how I accomplished it.

<a href='http://www.youtube.com/watch?feature=player_embedded&v=wxWo-WlLwhA' target='_blank'><img src='http://img.youtube.com/vi/wxWo-WlLwhA/0.jpg' width='425' height=344 /></a>

http://www.imo.net/radio/reflection

# Details #

Things you'll need:
  * A RTL Dongle (I prefer the Nooelec R820T) but likely any will be ok.
  * Antenna (a directional antenna will be useful, but anything will work) I use a 6 Ele 50Mhz Yagi at 15 feet up.
  * Coax (better is gooderer :-)  I already had LMR400 on this antenna.
  * Not required, but I use a Miteq LNA 'AU-2A-0110' and sometimes a Miteq 'AU-1362'
  * SOFTWARE:
    * SDR#
    * Zadig.exe
    * Spectrum Lab
      * script for spectrum lab to do the automated detection process.
    * Colorgramme

## SOFTWARE SETUP ##

### SDR# ###
http://sdrsharp.com/index.php/downloads
  * INSTALLATION:**http://rtlsdr.org/softwarewindows**

![https://cdar.googlecode.com/files/sdrms1.jpg](https://cdar.googlecode.com/files/sdrms1.jpg)

![https://cdar.googlecode.com/files/sdrms2.jpg](https://cdar.googlecode.com/files/sdrms2.jpg)

![https://cdar.googlecode.com/files/sdrms3.jpg](https://cdar.googlecode.com/files/sdrms3.jpg)

![https://cdar.googlecode.com/files/sdrms4.jpg](https://cdar.googlecode.com/files/sdrms4.jpg)

![https://cdar.googlecode.com/files/sdrms5.jpg](https://cdar.googlecode.com/files/sdrms5.jpg)

![https://cdar.googlecode.com/files/sdrms6.jpg](https://cdar.googlecode.com/files/sdrms6.jpg)

![https://cdar.googlecode.com/files/sdrms7.jpg](https://cdar.googlecode.com/files/sdrms7.jpg)

![https://cdar.googlecode.com/files/sdrms8.jpg](https://cdar.googlecode.com/files/sdrms8.jpg)

![https://cdar.googlecode.com/files/sdrms9.jpg](https://cdar.googlecode.com/files/sdrms9.jpg)

### Spectrum Lab: ###
http://www.qsl.net/dl4yhf/spectra1.html

http://cmhas.wikispaces.com/slmeteor (**required** script setup)

THIS WIKI COPY OF REQUIRED SCRIPT:
https://cdar.googlecode.com/files/0_MeteorLogger_SD_2012-06-09.TXT

### Colorgramme: ###
http://radio.meteor.free.fr/fr/en/logiciels.html#4