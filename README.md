# Neptune-4-Pro---Wipe-Brush
This is a mod to add a brass bristle brush so the nozzle can be physically cleaned before printing (or anytime it is requested via macro call).

The 3D Printed mount can only be 10mm wide otherwise the brush, which is mounted to the Bed, can't fit past the gantry.
The brush used is a common "$2 shop", "from China" brush that typically come in a set of three. One with brass bristles, one with stainless steel bristles, and another with nylon bristles. Some are different shapes, so if need be you migth have to do some brush hacking to only use 10mm width of it. These brushes tend to have 'plugs' of bristle groups and you can grab and pull out a 'plug' of them with cutters to grip them. They can be hard to cut off well, so pulling them out is better. The 3D Printed mount has holes to allow screwing up into the brush piece from below. The 'plug' holes are perfectly suited to use 2mm bolts to hol dthe brush down.

The brush mount is put in under the two left bed screws and it does not bother their operations. You don't have to remove the bed, just undo those two knows/screws totally and feed the mount onto the bed screw/bolts. The mount has an upper portion to help clamp the bed frame better, but it works OK without that too.

You need to edit your printer.cfg in a few ways. Change the [stepper_x] section, position_min = -14 and the position_endstop = -14
I recommend this as it sets the X=0 position to be over the printable PEI bed region, so then you can have a Slicer bed min as X=0 which is a more 'normal' sort of value to have as the furtherest left to print from(!).
Not related to this mod, I also use [stepper_y] postion_min = -4 and position_endstop = -4   This is again so that a Y=0 position is over the PEI bed, and you can set a Slicer to Y=0 as the min.

The macro moves the printhead down to Z=1 on my N4pro, but you really need to look and check your own system, and adjust it so that it does run the nozzle through the bristles, but not higher to hit the silicone boot.
It does 'three' wipes so that it ends up on the middle bed side of the brush and can then head straight to the mid bed print start region, in a short path to have less time to ooze filament again.

