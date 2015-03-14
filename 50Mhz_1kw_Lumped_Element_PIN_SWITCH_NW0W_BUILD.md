|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

Step-By-Step Detail on NW0W Build of the VK3OE TR PIN Switch.


# Construction Detail #

Steps Taken To recreate the Design [VK3OE modeled](https://cdar.googlecode.com/files/50Mhz_1kw_PIN_SWITCH.png) that is based on a hybrid of a 50kw NOAA T/R Switch and one built by SM5BSZ.
  * Purchased items in Table 1 of **...**

## Current ##
![https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj.jpg](https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj.jpg)
![https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_1.jpg](https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_1.jpg)
![https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_2.jpg](https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_2.jpg)
![https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_3.jpg](https://cdar.googlecode.com/files/hp_tr_ant_to_rx_port_swr_adj_3.jpg)

## Start to Current ##

  * **Building the Coils**
    * To wind the required 10mm diameter coils requires 14 AWG Magnet wire, which is wound around a 9mm form.  In my case I choose to use the shank of an old 23/64 Drill Bit which is very close to 9mm diameter.  This size plus the 14 AWG gauge wire creates the 10mm diameter coil requirement.
      * A photo of [the drill bit used is here](http://cdar.googlecode.com/files/23_64_9mm_drillbit.jpg).  I wrapped one layer of electrical tape around the shank of the drill-bit in order to not scratch the coating of the magnet wire in the coil area as I wound them.
      * Winding the coils is pretty straight forward, you simply wrap the wire around the drill-bit or 9mm form the number of turns required by the schematic.
    * Final product of the coils should look something like this.
> > > ![http://cdar.googlecode.com/files/tr_coil_side_view.jpg](http://cdar.googlecode.com/files/tr_coil_side_view.jpg)
> > > ![http://cdar.googlecode.com/files/tr_coils.jpg](http://cdar.googlecode.com/files/tr_coils.jpg)
> > > ![https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_1.jpg](https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_1.jpg)
> > > ![https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_2.jpg](https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_2.jpg)
> > > ![https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_3.jpg](https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_3.jpg)
> > > ![https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_4.jpg](https://cdar.googlecode.com/files/50Mhz_Self_Res_L13_L14_4.jpg)

![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%281%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%281%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%282%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%282%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%283%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%283%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%286%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%286%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%289%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%289%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2810%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2810%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2811%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2811%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2812%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2812%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2813%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2813%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2814%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2814%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2815%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2815%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2816%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2816%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2817%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2817%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2818%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2818%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2819%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2819%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2820%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2820%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2821%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2821%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2822%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2822%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2823%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2823%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2824%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2824%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2825%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2825%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2826%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2826%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2829%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2829%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2832%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2832%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2834%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2834%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2837%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2837%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2840%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2840%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2843%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2843%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2846%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2846%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2847%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2847%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2848%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2848%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2849%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2849%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2850%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2850%29.jpg)

![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2851%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2851%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2852%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2852%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2853%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2853%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2854%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%20%2854%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%2855%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%2855%29.jpg)
![https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%2856%29.jpg](https://cdar.googlecode.com/files/nw0w_build_vk3oe_1kw_pin_tr_switch_%2856%29.jpg)