In order to explore the far lands in the third dimension, we'll need the Cubic Chunks mod (and Cubic World Gen mod), along with my far lands mod. Once you have those installed, enable the far lands by heading to cubicworldgen\_mixin\_config.json and changing allow\_farlands\_worldgen to true.

To get these images, I used Cubic Chunks version 0.0.970.0, and Chunk World Gen version 0.0.39.1.

Currently, this mod restricts teleportation about a billion blocks behind the 32 bit integer limit. We can fix this with a couple of patches.

First, we would need to replace all instances of this limit. Go to the Github repository for Cubic Chunks (https://github.com/OpenCubicChunks/CubicChunks/) and search for MIN\_BLOCK\_Y and MAX\_BLOCK\_Y. Find them in the code (they will appear as integers) and replace with the 32 bit max and min integers.

Head to io/github/opencubicchunks/cubicchunks/core/asm/mixin/selectable/common/MixinWorld_SlowCollisionCheck.class. Replace all 3*10^7. Do the same for io/github/opencubicchunks/cubicchunks/core/asm/mixin/fixes/common/MixinNetHandlerPlayServer.class.

Lastly, go to io/github/opencubicchunks/cubicchunks/api/util/Coords.class at midPos(). Replace everything in the method with the following:

![CubicChunksMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/CubicChunksMod.png)

In the same folder where you see Coords.class, move CoordsFix.class there (in the assets/Ch4 folder).

Now, create a world with "Custom Cubic" as the type. Teleport up to (12550821, 25101642, 12550821), and you should see the vertex far lands. Remember that the sky far lands start at twice the limit where the edge far lands start.