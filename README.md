# 555-astable-multivibrator
555 astable multivibrator 

The circuit diagram of a 555 Timer wired in Astable Mode. 8th pin and 1st pin of the IC are used to give power, Vcc and GND respectively. The 4th pin is RESET pin which is active low and is connected to Vcc to avoid accidental resets. 5th pin is the Control Voltage pin which is not used. So to avoid high frequency noises it is connected to a capacitor C’ whose other end is connected to ground. Usually C’ = 0.01μF. The Trigger (pin 2) and Threshold (pin 6) inputs are connected to the capacitor which determines the output of the timer. Discharge pin (pin 7) is connected to the resistor Rb such that the capacitor can discharge through Rb. Diode D connected in parallel to Rb is only used when an output of duty cycle less than or equal to 50% is required. 
Since the Control Voltage (pin 5) is not used the comparator reference voltages will be 2/3 Vcc and 1/3 Vcc respectively. So the output of the 555 will set (goes high) when the capacitor voltage goes below 1/3 Vcc and output will reset (goes low) when the capacitor voltage goes above 2/3 Vcc.
# Working
	When the circuit is switched ON, the capacitor (C) voltage will be less than 1/3 Vcc. So the output of the lower comparator will be HIGH and of the higher comparator will be LOW. This SETs the output of the SR Flip-flop.
Thus the discharging transistor will be OFF and the capacitor C starts charging from Vcc through resistor Ra & Rb.


When the capacitor voltage will become greater than 1/3 Vcc ( less than 2/3 Vcc ), the output of both comparators will be LOW and the output of SR Flip-flop will be same as the previous condition. Thus the capacitor continuous to charge.
When the capacitor voltage will becomes slightly greater than 2/3 Vcc the output of the higher comparator will be HIGH and of lower comparator will be LOW. This resets the SR Flip-flop.
Thus the discharging transistor turns ON and the capacitor starts discharging through resistor Rb.
Soon the capacitor voltage will be less than 2/3 Vcc and output of both comparators will be LOW. So the output of the SR Flip-flop will be the previous state.
So the discharging of capacitor continuous.
When the capacitor voltage will become less than 1/3 Vcc, the output SETs since the output of lower comparator is HIGH and of higher comparator is LOW and the capacitor starts charging again.
This process continuous and a rectangular wave will be obtained at the output.
