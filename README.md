# 555-astable-multivibrator
555 astable multivibrator 

The circuit diagram of a 555 Timer wired in Astable Mode. 8th pin and 1st pin of the IC are used to give power, Vcc and GND respectively. The 4th pin is RESET pin which is active low and is connected to Vcc to avoid accidental resets. 5th pin is the Control Voltage pin which is not used. So to avoid high frequency noises it is connected to a capacitor C’ whose other end is connected to ground. Usually C’ = 0.01μF. The Trigger (pin 2) and Threshold (pin 6) inputs are connected to the capacitor which determines the output of the timer. Discharge pin (pin 7) is connected to the resistor Rb such that the capacitor can discharge through Rb. Diode D connected in parallel to Rb is only used when an output of duty cycle less than or equal to 50% is required. 
Since the Control Voltage (pin 5) is not used the comparator reference voltages will be 2/3 Vcc and 1/3 Vcc respectively. So the output of the 555 will set (goes high) when the capacitor voltage goes below 1/3 Vcc and output will reset (goes low) when the capacitor voltage goes above 2/3 Vcc.
# Working
	
