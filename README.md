# bfb-3dtouch
modding the bitsfrombytes 3d touch to be useful

TODO: images of the completed build

# Prelude

There once was a company called Bits From Bytes LTD, trying to revolutionize the 3D printer market with their proprietary 3D printers - with what they were actually quite successful.

They were so revolutionary that 3DSystems bought them back in 2010...
What happened afterwards? No support, no replacement parts, no opensourcing of the printer software and hardware,... - basically throw that thing [in the bin](https://www.youtube.com/watch?v=Y47PDT4coNE).

@3DSystems:

![Linus Torvalds "Fuck you Nvidia"](img/torvaldsnvidia.jpg)

# I have a working printer and do not want to modify it

- Use kisslicer, it is the only slicer which worked for me (do not use that shitty 3dsystems slicer, it does not work with *their* own hardware AND costs money.)
- Be careful with the Z-Axis, depending on how often your room temperature changes IT WILL BE OFF AND GRIND YOUR NOZZLE INTO THE BUILDPLATE.

# Specs

- Extruders: Up to 3, though really heavy on the x-y axis and something for the machining-art museum
- Total size: 51.5 x 51.5 x 59.8 cm
- Weight: ~ 36 kg (yes, it is a tank)
- Build Volume: up to 275 x 275 x 201 mm
- LCD touch screen (which is something I will not reverse engineer since it costs more time than throwing it in the bin.)

# Modifications

## Z-Axis
For the parts on the z axis I used some TODOmm sheet of aluminium using the original plexiglass parts which started to fail as templates.

For the buildplate i used that aluminium sheet too and (todo, still not done :) )

For the endstop I used a "thing i do not remember the name of from a hoverboard" and a piece of plastic on the z axis connection plate to break the light.

TODO: images and more info
### Hotplate
TODO

## Controller
For the controller I chose a MKS Tinybee - it is dirt cheap, has documentation, comes with trinamic drivers and has wifi.
![mks tinybee](img/mkstinybee.jpg)

### Standby power mod
Desolder D3 from the Tinybee and feed 12Vsb to the kathode pin. 

### PSU "enable" mod
In order for the Power Supply to be turned on when it is actually needed, hook up TODO on the tinybee to TODO on the power supply.

### Connectors
For reusing the connectors I just unclipped them from their original connectors and stuffed them into fitting JST plugs. 

Put some epoxy over it and you are done.

## Wiring
TODO

## Display
TODO

## Power Supply
For the power supply I chose a dirt cheap HP HSTNS-PL14.
![psu](img/psu.jpg)
It has +12Vsb as well as tons of amps on its output.
### Modifying output voltage
The power supply has a potentiometer to set the voltage, modify the resistor near it to TODO VALUE in order to be able to set the output voltage to 13.5V

TODO: OVP & OCP modification to 24v 

### Connectors
To make the PSU easily replacable I used some phoenix connect plugs (todo part number) which have a fitting female end with screw terminals.

### Power Monitoring
TODO, the psu should have I2C
