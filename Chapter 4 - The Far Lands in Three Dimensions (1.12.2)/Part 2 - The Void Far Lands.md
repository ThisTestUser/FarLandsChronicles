The void far lands are the mirror image of the sky far lands. Normally, negative Y values do not generate terrain, but with Cubic Chunks, the world generates all the way down to the lower integer limit.

The abundance of water will cause crashes in your world. To combat this, use a [mod](https://www.curseforge.com/minecraft/mc-mods/no-water-spread) that prevents water from spreading. Ensure you apply the commands ```/gamerule doWaterSpread false``` and ```/gamerule doLavaSpread false``` every time you create a new world.

Seed: -936504578442456880 (unless otherwise noted)

The edge far lands and corner far lands are below. Note the abundance of gravel placed by the terrain decorator.

![VEdge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VEdge.png)

![VCorner](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VCorner.png)

Here is the intersection of the 3 edges of the far lands, void version:

![VIntersect](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VIntersect.png)

Below are the void far lands, and then the void edge far lands. The terrain shape is the same as the sky far lands.

![VoidFar](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VoidFar.png)

![VoidEdge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VoidEdge.png)

Now let's look at the vertex far lands. Like from before, we'll consider this to be the normal type of terrain that generates here. The pockets are air are caused by falling gravel, and are not filled because water spread is turned off.

![VVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex1.png)

![VVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex2.png)

Blockiness in the terrain serves as an indicator that a transition to solid or empty terrain is close by. Below, we see a boundary from solid to blocky, which gradually transitions back to normal terrain.

![VVertex3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex3.png)

![VVertex4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex4.png)

![VVertex5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex5.png)

For the solid and empty types, the terrain generates stone everywhere and water everywhere respectively. Keep in mind that all non-cave air pockets are filled with water by default.

![VVertex6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex6.png)

![VVertex7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertex7.png)

Now let's look at some transitions between the variants. The same pattern seen in the sky far lands holds here also.

![VVertexT1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT1.png)

The following two images are proof that transitions extend across different corners.

![VVertexT2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT2.png)

![VVertexT3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT3.png)

The parallel transition depicted above eventually intersects with a diagonal transition in the ++ axis. Note that the terrain just before is not blocky. This is caused by the terrain becoming more normal just before the intersection.

Look closely at the following images and you'll also see the parallel transition go from normal <-> solid to normal <-> empty. The diagonal transition also changes types, but it is harder to see.

![VVertexT4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT4.png)

![VVertexT5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT5.png)

![VVertexT6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT6.png)

The below image is a transition whose coordinates correlate with a transition seen before in the sky far lands page. Note that a second transition can be seen parallel to the Y axis.

![VVertexT7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT7.png)

Moving in the +Z direction reveals a second intersection close by, parallel to the downwards transition seen before.

![VVertexT8](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT8.png)

By following the intersection towards the origin, we can see that we do not have two transitions, but one transition, which is offset at a certain Y value for some reason.

![VVertexT9](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT9.png)

![VVertexT10](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVertexT10.png)

The normal farther lands are shown below.

![VFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFarther1.png)

![VFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFarther2.png)

![VFarther3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFarther3.png)

Now we'll look at the blocky farther lands. Note the water pocket in the corner farther lands caused by a layer of gravel falling away.

![VFarther4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFarther4.png)

![VFarther5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFarther5.png)

With the solid and empty variants, the terrain extends across the farther lands boundary with no differences seen.

Now let's look at some transitions, but this time in the farther lands.

![VFartherT1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT1.png)

![VFartherT2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT2.png)

![VFartherT3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT3.png)

![VFartherT4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT4.png)

![VFartherT5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT5.png)

The transition depicted in the image above intersects with a diagonal transition. Like before, the two transitions swap types. This is more obviously seen than in the example before. Note that the farther lands are not blocky at the intersection.

![VFartherT6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT6.png)

![VFartherT7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT7.png)

![VFartherT8](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT8.png)

![VFartherT9](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT9.png)

Below, we are revisiting the intersection which we have seen before, except this time we are in the farther lands.

![VFartherT10](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT10.png)

![VFartherT11](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VFartherT11.png)
