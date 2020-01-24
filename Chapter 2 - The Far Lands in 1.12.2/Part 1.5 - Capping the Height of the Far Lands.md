The far lands were generated in a time where the height limit was only 128 blocks. In fact, re-enabling the far lands in 1.6.X would lead the terrain to stop generating at 128 blocks. However, in recent versions, the far lands take advantage of the 256 block height limit, generating all the way to the top. In order to get the real "feel" of the original far lands, we are going to cap the height through several modifications.

In net/minecraft/world/biome, change 255 to 127 in Biome, BiomeDecorator, BiomeMesa, BiomeSwamp. There should be one replacement per class.

Next, go to net/minecraft/world/gen/ChunkGeneratorOverWorld.java and replace 256 with 128. There should be four instances of this, including one where a number is defined as 256.0D. In `setBlocksInChunk`, replace 32 with 16.

In MapGenCaves and MapGenRavine (same package as above), replace 256 with 128.

In NoiseGeneratorImproved and NoiseGeneratorSimplex, replace every single instance of 256 and 255 with 128 and 127 (respectively). Also replace 512 with 256 in both files. There should be 13 replacements in NoiseGeneratorImproved and 12 in NoiseGeneratorSimplex.

Once these changes are done, the far lands should only extend to 128 blocks tall.

If you would like to limit structure generation to 128 blocks, you can replace all instances of 256 with 128 in the package net/minecraft/world/gen/feature.

![128](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/128.png)