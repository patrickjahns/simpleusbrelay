Simple Python Module for controlling usb relays
==================================

Description
-----------

This is a simple library for controlling usb relays using this windows library/utility for controlling
http://www.mediafire.com/download/m55ax4cddcshauq/USBRelayExtLib.rar

example:
http://www.ebay.de/itm/Brand-New-USB-Relay-2-Channel-Programmable-Computer-Control-For-Smart-Home-/161078781195

Dependencies
------------
simpleusbrelay uses pyusb to cummunicate with usb devices over python
check out the pyusb project ( https://github.com/walac/pyusb // http://pyusb.sf.net/)

Usage
-----

Install::

	pip install simpleusbrelay

Instantiate::

	import simpleusbrelay
	relaycontroller=simpleusbrelay(idVendor=16c0, idProduct=05df)

Turning relay x on/off::
	
	#x == relaynumber (between 1 - 8)
	relaycontroller.array_on(x)
	relaycontroller.array_off(x)

Turning all relays on/off::

	relaycontroller.array_on(all)
	relaycontroller.array_off(all)