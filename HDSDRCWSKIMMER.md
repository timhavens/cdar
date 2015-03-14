#Using HDSDR to Feed I/Q into CWSKIMMER

# Introduction #

http://www.reversebeacon.net/dxsd1/dxsd1.php?f=0&c=NW0W&t=de

If you so desire it's possible to route HDSDR I/Q signals out to CWSKIMMER.

In order to do this you will need the following.

**THIS IS NOT A COMPLETED MANUAL**
This is just a pointer to how I have set this up and have it running currently.  I'll add more descriptive text soon.

![https://cdar.googlecode.com/files/rtl_to_ftdx_block.jpg](https://cdar.googlecode.com/files/rtl_to_ftdx_block.jpg)

## HamItUp Method ##
<a href='http://www.youtube.com/watch?feature=player_embedded&v=P0ptFsM83Qo' target='_blank'><img src='http://img.youtube.com/vi/P0ptFsM83Qo/0.jpg' width='425' height=344 /></a>

## software required ##
  * LBP2 (serial port sharing for CAT control)
    * http://www.telepostinc.com/LPB2.html
  * Virtual Audio Cable
    * http://software.muzychenko.net/eng/vac.htm (**costs $35 for Full Versio**)
    * http://vb-audio.pagesperso-orange.fr/Cable/ (Free for one virt. cable - W9RM reports it seems to work with the same quality as VAC)
  * CWSkimmer
    * http://www.dxatlas.com/CwSkimmer/Files/CwSkimmer.zip
    * MasterData File
      * http://www.it9tyr.com/it9tyr/2013/04/6m-master-dta-database-2013/
        * To edit the master data file download and use (not a requirement but you'll probably want to edit the master data file from time to time to improve CWSKIMMER accuracy.
          * http://www.dxatlas.com/MEdit/
  * Aggregator 2.4 (**ONLY if you want to send spots to the Reverse Beacon Network**)
    * http://www.reversebeacon.net/genn.php?a=started

# Details #

## LBP2 Setup ##
![https://cdar.googlecode.com/files/LBP2_setup_share_cat.jpg](https://cdar.googlecode.com/files/LBP2_setup_share_cat.jpg)

![https://cdar.googlecode.com/files/omni_rig_rig2_for_cw_skimmer.jpg](https://cdar.googlecode.com/files/omni_rig_rig2_for_cw_skimmer.jpg)

## Virtual Audio Cable ##
![https://cdar.googlecode.com/files/virt_audio_cable_setup.jpg](https://cdar.googlecode.com/files/virt_audio_cable_setup.jpg)

![https://cdar.googlecode.com/files/audio_recording_devices.jpg](https://cdar.googlecode.com/files/audio_recording_devices.jpg)

![https://cdar.googlecode.com/files/vac_1_1.jpg](https://cdar.googlecode.com/files/vac_1_1.jpg)

![https://cdar.googlecode.com/files/vac_1_2.jpg](https://cdar.googlecode.com/files/vac_1_2.jpg)

![https://cdar.googlecode.com/files/vac_1_3.jpg](https://cdar.googlecode.com/files/vac_1_3.jpg)

![https://cdar.googlecode.com/files/vac_1_4.jpg](https://cdar.googlecode.com/files/vac_1_4.jpg)

![https://cdar.googlecode.com/files/hdsdr_cwskimmer_IQ.jpg](https://cdar.googlecode.com/files/hdsdr_cwskimmer_IQ.jpg)

![https://cdar.googlecode.com/files/hdsdr_virt_audio_setup.jpg](https://cdar.googlecode.com/files/hdsdr_virt_audio_setup.jpg)

## CW SKIMMER ##
![https://cdar.googlecode.com/files/cwskimmer_1.jpg](https://cdar.googlecode.com/files/cwskimmer_1.jpg)
![https://cdar.googlecode.com/files/cwskimmer_2.jpg](https://cdar.googlecode.com/files/cwskimmer_2.jpg)
![https://cdar.googlecode.com/files/cwskimmer_3.jpg](https://cdar.googlecode.com/files/cwskimmer_3.jpg)
![https://cdar.googlecode.com/files/cwskimmer_4.jpg](https://cdar.googlecode.com/files/cwskimmer_4.jpg)
![https://cdar.googlecode.com/files/cwskimmer_5.jpg](https://cdar.googlecode.com/files/cwskimmer_5.jpg)
![https://cdar.googlecode.com/files/cwskimmer_6.jpg](https://cdar.googlecode.com/files/cwskimmer_6.jpg)
![https://cdar.googlecode.com/files/cwskimmer_7.jpg](https://cdar.googlecode.com/files/cwskimmer_7.jpg)

## Aggregator ##
![https://cdar.googlecode.com/files/agg_1.jpg](https://cdar.googlecode.com/files/agg_1.jpg)
![https://cdar.googlecode.com/files/agg_2.jpg](https://cdar.googlecode.com/files/agg_2.jpg)
![https://cdar.googlecode.com/files/agg_3.jpg](https://cdar.googlecode.com/files/agg_3.jpg)
![https://cdar.googlecode.com/files/agg_4.jpg](https://cdar.googlecode.com/files/agg_4.jpg)
![https://cdar.googlecode.com/files/agg_5.jpg](https://cdar.googlecode.com/files/agg_5.jpg)
![https://cdar.googlecode.com/files/agg_6.jpg](https://cdar.googlecode.com/files/agg_6.jpg)