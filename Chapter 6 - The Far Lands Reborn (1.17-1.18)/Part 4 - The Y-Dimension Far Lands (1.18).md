In order to make the sky far lands appear, the Y-scale should be stretched to 196106.574487 (see Part 0). This allows the sky far lands to appear at Y=128. The sky far lands stop at Y=256, as that is the maximum height the terrain generator uses (features like trees will generate higher).

Interestingly, some mountain biomes cause the sky far lands to generate more sparsely.

![18SkyFar1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyFar1.png)
 
![18SkyFar2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyFar2.png)

The vertex far lands are as expected (more chaotic than the corner far lands), and the sky edge far lands consist of a long continous stone slab running to Y=256, also as expected.

![18SkyVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyVertex1.png)
 
![18SkyVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyVertex2.png)

![18SkyVertex3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyVertex3.png)

![18SkyVertex4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyVertex4.png)

As we move into the farther lands, it seems that the terrain gets much smoother, as expected.

![18SkyFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyFarther1.png)
 
![18SkyFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18SkyFarther2.png)

Now let's look at the void far lands (Y-Scale = 784426.297949). Below is how it looks without the aquifer fix.

![18VoidFar](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18VoidFar.png)

The void vertex far lands are as expected and can be thought of as the inversion of the sky vertex far lands.

![18VoidVertex](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18VoidVertex.png)

As we move into the farther lands again, the terrain smooths out, mirroring the sky vertex farther lands.

![18VoidFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18VoidFarther1.png)
 
![18VoidFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18VoidFarther2.png)

One interesting thing that happens is that large amounts of bedrock (but not the bottommost layer) are removed by the terrain generation. This doesn't seem to happen in 1.17.

![18BedrockErase1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18BedrockErase1.png)

As always, the terrain can vary a lot, depending on the seed and axis.

![18VoidFarther3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18VoidFarther3.png)

Now, the Y-scale is set to 62754103.8359. This makes the entire world contain only far lands.

![18YFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18YFarther1.png)

However, this does not make the farther lands appear in the void, as the farther lands start generating at Y=+/-64. Instead, the Y-scale is set to 125508207.672 to allow this to happen.

![18YFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18YFarther2.png)

Now as expected, the void far lands override the normal corner/edge far lands after Y=-32.

![18YFarther3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18YFarther3.png)

When all 3 farther lands intersect, nothing really interesting occurs.

![18YFarther4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18YFarther4.png)

The only real difference is that the bottom of the world has large amounts of bedrock removed.

![18BedrockErase2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/18BedrockErase2.png)
