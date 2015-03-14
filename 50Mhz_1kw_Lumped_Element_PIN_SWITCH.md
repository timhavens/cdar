|[Home](https://code.google.com/p/cdar/wiki/Home)|[Rack](https://code.google.com/p/cdar/wiki/RackMountSystem)|[Hermes](https://code.google.com/p/cdar/wiki/HermesSetup)|[LP-Pin](https://code.google.com/p/cdar/wiki/LowPowerPinSwitchTTL)|[HP-Pin-Driver](https://code.google.com/p/cdar/wiki/PIN_SWITCH_DRIVER)|[HP-PIN-TR](https://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH)|[GPSDO](https://code.google.com/p/cdar/wiki/GPSDO)|[HP-AMP](https://code.google.com/p/cdar/wiki/FastHighPower50MhzAmp)|[RF-Amp-Bay](https://code.google.com/p/cdar/wiki/RFAmpBay)|[Power-Bay](https://code.google.com/p/cdar/wiki/PowerBay)|[SDR-Bay](https://code.google.com/p/cdar/wiki/SDRBay)|[External](https://code.google.com/p/cdar/wiki/EnternalLinks)|
|:-----------------------------------------------|:----------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------------------------------------|:---------------------------------------------------------|:--------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|

# Introduction #

Monostatic Radar requires very high speed  TR (transmit/receive) switching.  The TR switch must have very high isolation between T and R components.  It must also have very LOW insertion loss.  Although the design we've settled on suites our requirements for this project, it is likely useful for MANY OTHER applications within the Amateur domain.

This design is a bit of a hybrid between an old TR Radar Switch from NOAA, and a newer version from SM5BSZ.  It was modeled by VK3OE (Andrew Martin).

# Initial Requirements #

**THIS IS THE CRUX OF MAKING Monostatic Radar WORK** We need a RF switch that has:

  * 1 COMM Port (antenna)
  * 2 Ports (TX and RX)
  * Can switch in <= .5mS
  * Can Handle 500W Average (1 sec ON @500W, 1 sec OFF)
  * Can Handle Billions of cycles **(this eliminates virtually all NON-PIN Diode switches 1yr = 31.5M sec)**
  * Can be easily reproduced by other Hams and used for other projects as well.
  * 2A +/- 15vdc (dual output) Supply min. [HP 62215E will be used](https://code.google.com/p/cdar/wiki/HP_62215E) and provides up to 3A! (cheap on Ebay!)

![https://cdar.googlecode.com/files/tx_rx_isolation_1kw_pin_switch.jpg](https://cdar.googlecode.com/files/tx_rx_isolation_1kw_pin_switch.jpg)
![https://cdar.googlecode.com/files/tx_rx_isolation_1kw_pin_switch_and%20ZX80_OFF.jpg](https://cdar.googlecode.com/files/tx_rx_isolation_1kw_pin_switch_and%20ZX80_OFF.jpg)

# NOTE #
This schematic mentions UM9145 these are actually **UM9415** PIN's

# Original Designs #

  * [NOAA 50Mhz PIN Switch TR](http://cdar.googlecode.com/files/50kw_peak_tr_switch_part_2.jpg) and [this](http://cdar.googlecode.com/files/50kw_peak_tr_switch_part_1.jpg)
  * [SM5BSZ 144Mhz PIN Switch TR](http://cdar.googlecode.com/files/page139%2BDUBUS%2BT7.pdf)

# Expectations of the switch we've choosen #

  * [VK3OE](http://qrz.com/db/VK3OE) model based on NOAA and [SM5BSZ](http://qrz.com/db/SM5BSZ) designs.
    * KEYUP time 500ns (nano-seconds)
    * KEYDOWN time 1.5us (micro-seconds)
    * Easily able to support 1kw
    * **these are WELL WITHIN the requirements we set out to have!**

![https://cdar.googlecode.com/files/50Mhz_1kw_PIN_SWITCH_v2_4.jpg](https://cdar.googlecode.com/files/50Mhz_1kw_PIN_SWITCH_v2_4.jpg)
  * [Full sized Schematic](https://cdar.googlecode.com/files/50Mhz_1kw_PIN_SWITCH_v2_4.jpg)
  * [VK3OE Early Prototype](http://cdar.googlecode.com/files/VK3OE_PROTOTYPE_50Mhz_1kw_PIN_SWITCH.jpg)
  * [NW0W Build Details](http://code.google.com/p/cdar/wiki/50Mhz_1kw_Lumped_Element_PIN_SWITCH_NW0W_BUILD)

# PARTS LIST Table 1. #

|Item Description|Vendor|Vendor Part #|Manufacturer Part #|Manufacturer|Price (usd)|Quantiy|Sub-Total (usd)|URL|
|:---------------|:-----|:------------|:------------------|:-----------|:----------|:------|:--------------|:--|
|8"x10"x2.5" Chassis Enclosure|Mouser|563-AC-1418|AC-1418|Bud Industries |$20.20|1 |$20.20|[here](http://www.mouser.com/ProductDetail/Bud-Industries/AC-1418/?qs=%2fha2pyFadug%252bNHhpHxZue9YCPW4XaW7r5ADtYqpMq5Q%3d)|
|8"x10" Chassis Plate|Mouser|563-BPA-1518|BPA-1518|Bud Industries |$8.80|1 |$8.80|[here](http://www.mouser.com/ProductDetail/Bud-Industries/BPA-1518/?qs=%2fha2pyFadui5YzNB0IuYfj1vCUVK15k91MN9EC%252bFMOpbLj9kWTgJng%3d%3d)|
|10W 5Ohm Wirewound Resister|Mouser|588-40J5R0E|40J5R0E|Ohmite|$1.88|2 |$3.76|[here](http://www.mouser.com/Search/ProductDetail.aspx?R=40J5R0Evirtualkey58810000virtualkey588-40J5R0E)|
|Multilayer Ceramic Capacitors 220pF 1000V 5%|Mouser|77-VJ1206A221JXGAT5Z|VJ1206A221JXGAT5Z|Vishay/Vitramon|$0.98|2 |$1.96|[here](http://www.mouser.com/ProductDetail/Vishay-Vitramon/VJ1206A221JXGAT5Z/?qs=sGAEpiMZZMsh%252b1woXyUXj4yI8nSxAOIUHiX6%2fxSbSec%3d)|
|Multilayer Ceramic Capacitors 27pF 1000V 5%|Mouser|77-VJ1812A270JXGAT|VJ1812A270JXGAT|Vishay/Vitramon|$0.41|7 |$2.87|[here](http://www.mouser.com/ProductDetail/Vishay-Vitramon/VJ1812A270JXGAT/?qs=sGAEpiMZZMsh%252b1woXyUXj0kotir8RUQCCw26kZj%252bEXg%3d)|
|1kw PIN Switch Diode|RFParts|UM9415|UM9415|Microsemi|$9.75|2 |$19.50|[here](http://www.rfparts.com/catalogsearch/result/?q=UM9415)|
|CAPACITOR TRIMMER 6PF-55PF, 250V, THD|Newark|94F7411|94F7411|Johanson Manuf.|$2.20|2 |$4.40|[here](http://www.newark.com/johanson-manufacturing/9305/capacitor-trimmer-6pf-55pf-250v/dp/94F7411?Ntt=94F7411)|
|Magnet Wire 14 AWG|Ebay|14AWG|- |- |$4.60|1 |$4.60|[here](http://www.ebay.com/itm/Magnet-Wire-14-AWG-Gauge-Enameled-Copper-2oz-155C-10ft-Magnetic-Coil-Winding-/261087230857?pt=LH_DefaultDomain_0&hash=item3cca02fb89)|
|N Female Bulkhead Connector (x1,x2)|Ebay|- |- |- |$3.29|2 |$6.58|[here](http://cgi.ebay.com/ws/eBayISAPI.dll?ViewItem&item=370658907688&ssPageName=ADME:L:OU:US:3160)|
|SMA Female Bulkhead Connector (x3)|Mouser|523-132137|132137|Amphenol Connex|$5.05|1 |$.05|[here](http://www.mouser.com/ProductDetail/Amphenol-Connex/132137/?qs=sGAEpiMZZMuLQf%252bEuFsOrjqedbXhavPYi9AUrhh%252bvEo%3d)|
|Insulated Feed Through (x4)|Ebay|570-1795-02|570-1795-02|Cambion|$0.60|2 |$1.20|[here](http://cgi.ebay.com/ws/eBayISAPI.dll?ViewItem&item=220768415094&ssPageName=ADME:L:OC:US:1120)|
|FR4 PCB 8"x10"|Mouser|590-515|515|MG Chemicals|$10.94|1 |$10.94|[here](http://www.mouser.com/ProductDetail/MG-Chemicals/515/?qs=%2fha2pyFadugO9NaR%2fYYGOS4MCX7yM9vGKtIr9C9cOwM%3d)|
|**TOTAL**|  |  |  |  |  |  |$82.74|- |


**STILL WORKING ON THIS LIST**

|DESC|VENDOR|MOUSERPART|OEMPART|MANUFACTURE |$PRICE|QTY|$SUBTOTAL|[here](URL.md)|
|:---|:-----|:---------|:------|:-----------|:-----|:--|:--------|:-------------|

# Images #

![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%281%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%281%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%282%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%282%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%283%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%283%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%284%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%284%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%285%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%285%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%286%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%286%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%287%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%287%29.jpg)
![https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%288%29.jpg](https://cdar.googlecode.com/files/high_power_50Mhz_tr_switch_testing%20%288%29.jpg)