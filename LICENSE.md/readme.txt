This MSP430 assembly language program demonstrates using the MSP430 Universal Serial
Interface (USI) to send data to an external LED display. It was assembled under
the IAR Embedded Workbench development environment but should be easily portable to
other assemblers. The program shows a 12 hour clock on an LED dot matrix display,
which has 8 rows and 24 columns. The code is written for the MSP430G2231 processor and
runs on a Texas Instruments LaunchPad evaluation board. Other MSP430 processors that have
the USI logic should also work, as long as they have at least 2k of program EPROM.

Please note the following hardware requirements:

	1.	The selected display uses Maxim MAX7219 ICs to control three 8X8 LED modules
	2.	The SPI output to the display has 3.3 volt logic. A TTL (5V) level converter
		must be inserted between the LaunchPad output pins and the display.
	3.	There are three switches for setting the time. They all require pull-up resistors
		to 3.3V, with a value of between 5k and 47k.
	4.	The data from the SPI input isn't used, so the pin could simply be terminated.
	5.	The on-board LED on P1.0 is used to indicate PM times. If you choose to use
		an external LED, you must add a 470 Ohm current limiting resistor.
	6.	The LaunchPad board must have the 32 kHz crystal and associated capacitors
		installed for accurate time display. 