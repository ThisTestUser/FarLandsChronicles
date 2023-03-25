Before we start using mods, there are actually a couple of Far Lands-related phenomena that can be observed in a completely vanilla install of 1.12.2 simply via the use of customized worlds.

Firstly, it's quite easy to encounter the Overworld's sky Far Lands (discussed in further detail in part 2) simply by setting the heightScale of a Customized world to a sufficiently high value. The lowest such value that generates sky Far Lands is 69273664. If heightScale is set to a value 69273656 or lower, sky Far Lands will not generate. Note that heightScale, like many other values in customized presets, is handled as a float, so at this point it's not possible to be any more precise than increments of eight.

![SkyFarLandsVanilla](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SkyFarLandsVanilla.png)

There are also interesting things to be seen via changing the coordinate scale value as well, which are discussed in depth in Chapter 5. If we set coordinateScale to exactly 532676640, nothing Far Lands-related will be immediately obvious. However, if we then teleport to exactly 2097152 blocks on one axis, we can encounter a thin wall bearing a very familiar shape.

![SheetsOneAxis](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SheetsOneAxis.png)

These occur on both the X and Z axis, so teleporting that distance on both axes expectedly yields a region where they intersect.

![SheetsTwoAxes1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SheetsTwoAxes1.png)

Teleporting twice the distance of these walls will reveal more walls which are almost exactly the same as the first, down to the very shapes of the holes:

![SheetsTwoAxes2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SheetsTwoAxes2.png)

Note that these walls will only occur in the positive directions: no walls exist at all in the negative-negative quadrant of the world.

If we change the coordinateScale by increments of 32 (the minimum possible value you can change a float of this magnitude by), the positions of the walls will shift also. Increasing the coordinateScale by 32 to a value of 532676672 will cause the first wall to generate at 1048576 (2097152/2) blocks out. Adding another 32 to the coordinatescale to make it 532676704 causes the first wall to appear at 699050 (2097152/3), and so on. No walls will generate if we go down by 32 from the first value (i.e. a coordinate scale of 532676608), which could be interpreted as them starting at a distance of 2097152/0, i.e. infinity.
