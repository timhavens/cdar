# Introduction #

To insure that you are using the correct sampling rate for your RTL dongle you may want to test it on your computer.  This shows how you can find out the fastest sampling rate your PC & RTL combo can handle.

Basically you don't want any or very very little loss.

The next three images show the test results on my very fast PC using an R820T dongle from China:

**3.2msps FAIL**
![https://cdar.googlecode.com/files/rtlsdr_test_1.jpg](https://cdar.googlecode.com/files/rtlsdr_test_1.jpg)

**2.88msps FAIL**
![https://cdar.googlecode.com/files/rtlsdr_test_2.jpg](https://cdar.googlecode.com/files/rtlsdr_test_2.jpg)

**2.4msps SUCCESS!**
![https://cdar.googlecode.com/files/rtlsdr_test_3.jpg](https://cdar.googlecode.com/files/rtlsdr_test_3.jpg)

# Details #

http://sdr.osmocom.org/trac/attachment/wiki/rtl-sdr/RelWithDebInfo.zip

Download that put in a directory of it's own I put mine here: **C:\Program Files\RTL\_SDR**

Open a command prompt

then try these in this order

ctrl-c (control C) exits the test.

If you see an continous 'lost at least' message hit CTRL and C to cancel and try the next level below:

  * 3.2msps
    * C:\Program Files\RTL\_SDR>rtl\_test -s 3.2e6
  * 2.88msps
    * C:\Program Files\RTL\_SDR>rtl\_test -s 2.88e6
  * 2.4msps (_this is the one I am now using because the previous two show lost data packets, and you don't want that_)
    * :\Program Files\RTL\_SDR>rtl\_test -s 2.4e6

This will tell you if your loosing any data when running at higher speed sampling rates.