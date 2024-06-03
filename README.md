Design files (Altium) for my bidirectional active rectifier. 

A Cortex-M4-driven bidirectional AC-DC power converter (active rectifier). 300W, 48VDC, 12VAC rms (through mains freq. step-down transformer). It should also be able to absorb/provide AC reactive power too. Its aim is more to be a test platform for control software than a useful/economical PSU. 

As of 2024-06-02, changes have been made to the inverter board but not incorporated into Altium because of a lack of license. They are:
 - PWModulator comparator output has been connected to GPIO PA.10 to measure duty cycle via a timer
 - U17, R56 and C87 have been removed as duty cycle is now measured digitally by a timer
 - R69 and R70 have been changed to 47 Ohm to improve rise time dramatically
 - R74, R76, R79 and R83 have all been changed to 1 Ohm to improve the power MOSFET's turn-off time