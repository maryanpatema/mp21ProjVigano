# mp21ProjVigano

Project Title:
HANDLING MULTIPLE EXTERNAL INTERRUPTS


Description:
All pins in ATmega328p can trigger interrupts when there is a change of state. However, only INT0 and INT1 can be configured to trigger interrupts in a low level. This trigger continuous until the low-level stops. Upon activation of these interrupts, the MCU gets ‘interrupted’ on what is it currently performing and jumps to execute the interrupt service routine.
		
Thus, the non-interrupt pins serve as an interrupt handler. This allows either INT0 or INT1 handle multiple external interrupts connected to their respective handlers. The pins are grouped into three ports that can serve as an interrupt vector, so the interrupt will trigger if any pin on that vector changes state, and has interrupts enabled.

Lastly, note that the processor follows a hierarchy when handling interrupt signals.  It handles and acts upon from the highest to least priority. 
