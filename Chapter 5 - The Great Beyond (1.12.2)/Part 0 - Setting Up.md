In this part, we will be exploring the fartherer and farthest lands. To start off, decompile 1.12.2 with ModCoderPack. We will be hanging around spawn this time, so we don't need to extend the world border.

First, let's go to net/minecraft/world/gen/ChunkGeneratorOverworld at provideChunk(). Modify the terrain generator to be like this:

![ChunkGen](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/ChunkGen.png)

(Note that caves/structures will NOT be offset.)

You will soon see a bunch of errors pop up. Try to Eclipse's quick fixes to fix them faster. You will need to modify local variable types (int to long) and two fields (BiomeCache). You will also need to cast to int at GenLayerIsland, GenLayerVoroniZoom, and GenLayerZoom.

In total, you should have changed 24 files. They are Biome, BiomeCache, BiomeProvider, ChunkGeneratorOverworld, the files in net/minecraft/world/gen/layer, and NoiseGeneratorOctaves.

Now that you have done that, you can change the long values at `xOff +=` and `zOff +=`. These are your "offsets". The values are then divided by 16, because we are offsetting chunk coordinates.