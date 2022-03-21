# AD8232-ECG-Module-with-Arduino-Heart-Rate-Monitor
AD8232 ECG Module with Arduino – Heart Rate Monitor


Red: RA (Right Arm)
Yellow: LA (Left Arm)
Green: RL (Right Leg)


ECG module is powered by connecting a power supply of 3.3 V at power pins.
A set of biomedical electrodes connecting wires having 3 electrode pads at one end and
a 3.5 mm male jack at the other end is used to carry electrical activity of the heart to the AD8232 module.
3 sensors are connected at the left arm, right arm, and right leg as per the color scheme.
The data received through the above-mentioned wires appear as an analog signal at the OUTPUT pin of module AD8232. 
This analog signal can be fed at the analog input pin of the microcontroller for further processing or visualization as a graph.
LO- and LO+ are connected to digital input pins of the microcontroller to check whether a sensor is connected or not.
~SDN is connected to the digital output pin of the microcontroller to activate the low power mode of module AD8232.


RA (Right ARM)
RA is the negative input (-IN) of the instrumentation amplifier of IC AD8232. A signal from the electrode connected to the right arm of the human body is received here.

RL (Right LEG)
RL is a green color biomedical electrode acts as an electrode input and connected to the right leg of the human body.

3.5 mm Female Biomedical Electrode Connector Jack
This connector has been provided as an alternate of RA, LA, RL pins. 
We can connect three electrodes to this connector instead of RA, LA, and RL pins using a 3.5mm male jack. 
There are two methods to detect the heartbeat: the two-electrode method and Three electrode method. 
Two Electrodes method uses the AC signal, and the Three Electrodes method uses DC signal. 
To detect which method is being used, LEAD OFF DETECTION is implemented in this module.

LO+	
Lead OFF Positive::
In DC Lead Off Detection mode, LO+ is LOW when electrode at +IN (of IC AD8232), i.e., LA (of module AD8232) is connected, 
and LO+ is HIGH when electrode at +IN (of IC AD8232) i.e. LA (of module AD8232) is disconnected. 
In AC Lead Off Detection mode, LO+ is LOW when electrodes at both +IN and –IN (of IC AD8232) i.e. LA and RA (of module AD8232) are connected, 
and LO+ is HIGH when the electrode at LA or RA is disconnected.

LO-
Lead OFF Negative::
In DC Lead Off Detection mode LO- is LOW when electrode at –IN (of IC AD8232) i.e. RA (of module AD8232) is connected
and LO- is HIGH when electrode at –IN (of IC AD8232) i.e., RA (of module AD8232) is disconnected. In AC Lead Off detection mode LO- is always LOW.

OUTPUT	
This is an output pin at which a filtered analog signal is present, and it gives the electrical activity of the heart.
This signal can be feed as an analog input to the Analogue to digital converter or microcontroller for analysis and visualization.


