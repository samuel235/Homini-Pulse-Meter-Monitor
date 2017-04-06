# Homini Pulse Meter Monitor

## Brief Description
This ATMEGA328P based board has been created to enable wireless monitoring of your power meter. The product comprises of two parts, one sensor attachment and one custom ATMEGA328P board that the sensor connects to. Both parts are enclosed inside of their own 3D printed enclosures to ensure safety to the devices.

This device has been designed to be located directly on your power meter, the sensor is stuck to the front and the controller is enclosed off to the side of the meter, designed to stick to the side also with Velcro, but you can put it where you wish. The sensor module is attached to the Controller device via a MicroUSB connector but obviously this can be modified to suit your personal needs.

As the module is running with an external 16MHz crystal, we are able to use MYSBootloader to enable us to use OTA Firmware Updates, saving you from having to physically get the module for a software/firmware update. We have also allowed the use of a ATSHA204 hardware signing by including a footprint for the ATSHA204 IC on the controller board.

## Function
- To monitor power usage of your home and report back to controller software for a visible display of your consumed electricity.

## Physical Dimensions
- Sensor: 36mm x 24mm x 33mm (Width x Length x Height)
- Controller: TBA

## Connectors
- FTDI and SPI for firmware upgrades
- Micro USB for Powering the device
- Micro USB for sensor connection

## Connections
#### Radio Frequency
Footprints for the following radios will be included.
- nRF24L01 Radio Transceiver
- RFM69 Radio Transceiver

## Power Supply
##### Either of the following:
- Micro USB wall charger.
- CR2450 Coin-cell battery.

## Software
#### Bootloader
- Mains Powered: MYSBootloader running at 16MHz External Crystal to enable the use of OTA updates.
- Battery Powered: MYSBootloader running at 8MHz Internal or External to enable the use of OTA updates.

#### Fuses
##### External Crystal (8MHz OR 16MHz):
- low_fuses=0xF7
- high_fuses=0xDA
- extended_fuses=0x06

##### Internal Crystal (8Mhz only) with Brown-out detection at 1.8v, best option for battery powered device:
- low_fuses=0xE2
- high_fuses=0xDA
- extended_fuses=0x06

#### Sketch

Will update sketches once I receive PCBs to test different variants of software out:

[Generic pulse sensor sketch Located here](https://www.mysensors.org/build/pulse_power), alternatively you can find customised sketches on my [github](https://github.com/samuel235/Homini-Pulse-Meter-Monitor)

## Testing
Testing will commence once boards have been received and assembled.

[//]: # "1.  - **COMPLETED**"
[//]: # "2.  - **COMPLETED**"

## TO-DO List
1. Order PCBs -
2. Assemble and test all PCBs -

## Update Log:
- Micro-Controller board designed (25/03/17)
- Sensor board designed (15/03/17)
- Sensor board (battery) designed (06/04/17)

## Issues
1. No issues reported at current date.

## Appreciations
Special thanks to:
1. Scalz from the MySensors community that has provided relevant design files and circuit schematics to aid in this product design. [MySensors](https://forum.mysensors.org/user/scalz)/[github](https://github.com/scalz)
2. [Mysensors.org](Mysensors.org)
3. [Openhardware.org](Openhardware.org)
4. [Sparkfun](sparkfun.com) and [Adafruit](adafruit.com) for their parts library for Eagle

If you have any suggestions, please add to the forum post over at [MySensors forum post]()

Please join in with the forum post at [MySensors](https://forum.mysensors.org/topic/6398/current-sensing) if you have any input on the topic of electricity monitoring.

I'm very interested in all of your variations, improvements and applications of this module, please add them to the comments with pictures and/or Videos.

## Disclaimer
**_I do not advise you in any way to make/install this product into a property and therefore I take no responsibility for any issues, problems you have or even health implications that you endure while completing the installation or even using the product after installing. BUILD, USE and INSTALL AT YOUR OWN RISK_**

## Licensing
This product is licensed under the CC-BY-SA OpenHardware certificate. For more information please see https://creativecommons.org/licenses/by-sa/4.0/
