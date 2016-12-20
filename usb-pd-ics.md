# USB PD type-C controllers
All prices are from Digikey.
## Desired characteristics:
* Want USB PD 2.0
* Support for being a downstream facing port (DFP) - those are for peripherals, versus upstream facing ports (UFP)
* Need ESD protection on all pins in use

## TI
### TPS25741
#### $3.20 at 1 quantity
* Source only
* -40℃ to 125℃
* More pins then TPS25740
	* ```!AUDIO``` - indicate audio device attached
	* ```!DEBUG``` - indicate debug device attached
	* ```GDPG``` (drive PMOS power switches)
	* ```PCTRL``` - control power advertised
	* ```!POL``` - something internal
* Honestly, not too sure what the difference is otherwise

### TPS25740
#### $3.25 at 1 quantity
* Source only
* -40℃ to 125℃

## Microchip
### UTC2000
#### $0.99 at 1 quantity
#### $1.14 at 1 quantity for -40 to 85℃
### UPD1001 (unavailable on Digikey)
### UPD1002
#### $1.76 at 1 quantity

## NXP
### PTN5100D
#### $2.00 at 1 quantity
Functional blocks:

* **Type-C Configuration Channel** functional block
	* orientation detection, cable/plug insertion, removal detection
* **USB PD** function
	* implements USB PD PHY and HW intensive protocol functions
	* discrete MCU provides full PD functionality (over SPI or I2C0
	* Either PD consumer or PD consumer/provider
	* PHY layer functions:
		* all sorts of bit transmission and CRC and stuff
	* Protocol layer functions
		* data packetization
		* CRC
		* etc.
* **Power FET** enable control
	* three dedicated open drain IOs to control external power MOSFETs
		* **EN_USBSRC** - enable/disable power MOSFETs that correspond to VBUS source (e.g. 5V regulated output).
		* **EN_USBFET1** - enable/disable power MOSFETs corresponding to USB PD power from external or delivering VBUS to external.
		* **EN_USBFET2** - enable/disable power MOSFETs corresponding to USB PD power from external or delivering VBUS to external.
* **MCU interface** and control

### PTN5150
#### $0.88 at 1 quantity
* Requires an external MCU to control it over I2C
* Only interfaces with CC1 pins

## Fairchild
### FUSB300C
#### $1.43 at 1 quantity
* 9-ball WLCSP (wafer-level chip scale package, aka ball grids, so unusable by hand)
* VBUS, CC1, CC2, GND pins for USB-C
* Interact with MCU over I2C and interrupt pin
* VCONN and VDD pins
* Great cheap CC PHY in a tiny package but unusable

### FUSB302
#### $1.06 at 1 quantity
### FUSB302B
#### $1.20 at 1 quantity

## Cypress
I think all of their offerings have integrated microcontrollers.
## STM
I think all of their offerings have integrated microcontrollers.