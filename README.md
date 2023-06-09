# rgb_laser_systems.py
A python package to control RGB Laser Systems lasers

To use this package, create a RGB_Laser object, this will establish communications with the laser. The laser can be connected either using the COM Port directly ("COM7", etc.) or it can connect using the serial number of the laser found in LTune: 
![Ltune Software serial number location](rgb_laser_systems/Ltune.png)

Basic Usage: 

```
laser=RGB_Laser("809392")
laser.set_outputPower(5) #In units of mW
laser.enable() #Starts the emission output, there is a 7 Sec safety delay before the laser starts
power=laser.get_outputPower() #Returns the output power of the laser in mW.
laser.set_outputPower(50) #Power can be changed at anytime without re-enabling the laser
laser.disable() #Disables the emission output
```
