# mp21ProjVigano


# Project Title: HANDLING MULTIPLE EXTERNAL INTERRUPTS

	Description:

	All pins in ATmega328p can trigger interrupts when there is a change of state. However, only INT0 and INT1 can be configured to trigger interrupts in a low level. This trigger continuous until the low-level stops. Upon activation of these interrupts, the MCU gets ‘interrupted’ on what is it currently performing and jumps to execute the interrupt service routine.

	Thus, the non-interrupt pins serve as an interrupt handler. This allows either INT0 or INT1 handle multiple external interrupts connected to their respective handlers. The pins are grouped into three ports that can serve as an interrupt vector, so the interrupt will trigger if any pin on that vector changes state, and has interrupts enabled.

	Lastly, note that the processor follows a hierarchy when handling interrupt signals.  It handles and acts upon from the highest to least priority. 




REFERENCES: 	
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


		M. A. Mazidi and S. Naimi. "#11 ATMEGA328P External Interrupts." Internet: https://www.arxterra.com/11-atmega328p-external-interrupts/, Aug. 22, 2018 [Mar. 25, 2021].
		
		M. A. Mazidi and S. Naimi. "The AVR Microcontroller and Embedded Systems using Assembly and C." Internet: http://web.csulb.edu/~hill/ee346/Lectures/10%20ATmega32U4%20Interrupts.pdf, Feb. 2009 [Mar. 23, 2021].
		
		EXTERNAL INTERRUPTS ON THE ATmega168/328.” Internet: https://sites.google.com/site/qeewiki/books/avr-guide/external-interrupts-on-the-atmega328?fbclid=IwAR1oAhzw4pPMl4eJ_mef_ILE1s0E-V8vUpGPbQugrrLOXkq1LVP4DN4YmNM, [March 25, 2021]

		Y. Kardid. “External interrupt on atmega328p.” Internet: https://Electronics.Stackexchange.Com/q/324891. https://electronics.stackexchange.com/questions/324891/external-interrupt-on-atmega328p?fbclid=IwAR20OJR_OU4mWBzYnMZ0txxrBlWV7NEGz6kHAzwJ5ZWvLqI9QkdjPWjhf_c, August 20, 2017 [March 25, 2021]
		
		J. M. Fiore. "29.2: External Interrupts." Internet: https://eng.libretexts.org/Bookshelves/Computer_Science/Book%3A_Embedded_Controllers_Using_C_and_Arduino_(Fiore)/29%3A_Bits_and_Pieces__Interrupts/29.2%3A_External_Interrupts, Sep. 2, 2020 [Mar. 25, 2021].
		
		"Global Manipulation of the Interrupt Flag." Internet: https://www.nongnu.org/avr-libc/user-manual/group__avr__interrupts.html, Feb. 8, 2016 [Mar. 25, 2021].


TEAM VIGANO:
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 	Ishmaiah Julia Agbay
	Andrea Therese Rodgrigo, Rapporteur
	Marianne Fatima Valenzuela, Team Lead
		


TABLE OF CONTENTS
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

	I.	INTRODUCTION

	II.	DISCUSSION

	a.	ATMEGA 328p 
	a.1. Features
	a.2. Pin Configurations and Description
	a.3. I/O Ports

	b.	Interrupts
	b.1. Basics of Interrupts
	b.2. Kinds of Interrupts
	b.3. Purpose of Interrupts
	b.4. Interrupt Service Routine

	c.	ATMEGA328p External Interrupts
	c.1. Interrupt Vectors in ATmega328P
	c.2. Register Description
		c.2.1. External Interrupt Control Register
		c.2.2. External Interrupt Mask Register
		c.2.3. External Interrupt Flag Register
		c.2.4. Pin Change Interrupt Control Register
		c.2.5. Pin Change Interrupt Mask Register
		c.2.6. Pin Change Interrupt Flag Register
	c.3. External Interrupt Processing
	c.4. Global Manipulation of the Interrupt Flag

	III.	CIRCUIT CONFIGURATIONS

	a.	Basic LED Toggle State
	a.1. Using One Pushbutton as an External Interrupt
	a.2 Connecting Multiple Pushbuttons in one External Interrupt
	a.3 Connecting Multiple Pushbuttons in all External Interrupt

	b.	Basic Binary Counter
	b.1. Using One Pushbutton to Count Up
	b.2. Using One Pushbutton to Count Up and Another to Reset Counting

	IV.	PROGRAMMING 

	a.	Basic LED Toggle State
	a.1. Using One Pushbutton as an External Interrupt
	a.2 Connecting Multiple Pushbuttons in one External Interrupt
	a.3 Connecting Multiple Pushbuttons in all External Interrupt

	b.	Basic Binary Counter
	b.1. Using One Pushbutton to Count Up
	b.2. Using One Pushbutton to Count Up and Another to Reset Counting

	V.	REFERENCES
	VI.	APPENDIX

WORK DISTRIBUTION
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

	INTRODUCTION: AGBAY
	DISCUSSION: (a) AGBAY, (b&c) RODRIGO
	CIRCUIT CONFIGURATIONS: (a) AGBAY, (b) RODRIGO
	PROGRAMMING: VALENZUELA

		
