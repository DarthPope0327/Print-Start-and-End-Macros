# Print-Start-and-End-Macros

You will need to replace any current print start and end macros in your .cfg files with these. Go through and uncomment the parts you will need based on your printer build.

In your slicer you will need to replace the machine start gcode with the following.

M104 S0 ; Stops Slicer from sending temp waits separately
M140 S0
print_start EXTRUDER=[first_layer_temperature] BED=[first_layer_bed_temperature] CHAMBER=[chamber_temperature]

In slicer you will need to replace the machine End gcode with the following.

PRINT_END

![Screenshot 2025-01-26 103829](https://github.com/user-attachments/assets/bcebcf31-c6cf-4c6d-9343-ab98123b2001)
