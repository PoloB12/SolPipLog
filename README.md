# SolPipLog

**Logger for the PIP Inverter series ( USB version )**

- working on 32bit UBUNTU / MATE.
- no Windows version yet
- sends data to [Emoncms](https://emoncms.org) 

 Emoncms is an open-source web application for processing, logging and visualising energy, temperature and other environmental data and is part of the [OpenEnergyMonitor project](http://openenergymonitor.org).

- sends data to [PVOutput](http://www.pvoutput.org).

 PVOutput is a free service for sharing and comparing PV output data.

## Install
 * copy file **"solpiplog.rules"** to your **"/etc/udev/rules.d/"** directory. That way you dont have to excecute it as root
 * make **solpiplog** executable with
   * **sudo chmod +x solpiplog** or 
   * change it with graphical interface inside of Ubuntu / Mate. Right click on file - properties - permissions tab - tick execute allow excecuting file as program
 * create an account on [Emoncms](https://emoncms.org) or install **Emoncms** on your own server. 
 * optional: create an account on [PVOutput](http://www.pvoutput.org).
 * configure **SolPipLog** with your Emoncms API-Key
  * optional configure **SolPipLog** with your PVOutput SystemID and API-Key.
  
## Values sent to Emoncms

Following values are sent to *Emoncms* and displayed as Node 30 with Key from 1-17

* 1  = AC_IN_V
* 2  = AC_IN_HZ
* 3  = AC_OUT_V
* 4  = AC_OUT_HZ
* 5  = AC_OUT_VA
* 6  = AC_OUT_W
* 7  = AC_OUT_LOAD_PERCENT
* 8  = BUS_V
* 9  = BATT_V
* 10 = BATT_CHRG
* 11 = BATT_CAPACITY_PERCENT
* 12 = HEATSINK_TEMP
* 13 = PV_I_BATT
* 14 = PV_V
* 15 = BATT_V_SCC
* 16 = BATT_DISCHRG_I
* 17 = PV Charging Power

## Values sent to PVOutput
Following values are sent to *PVOutput*

* AC_OUT_V
* AC_OUT_W
* PV Charging Power
