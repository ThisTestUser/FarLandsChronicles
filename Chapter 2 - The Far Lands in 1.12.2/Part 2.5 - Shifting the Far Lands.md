The far lands generate at an inconvenient place that makes it hard to play in. Even in 1.12.2, there are still many issues with generating terrain too far out from spawn. We can change the coordinate scale so the far lands start very close to spawn, but we end up damaging the terrain. Here, we will shift the far lands to spawn without messing with the terrain itself.

We'll start at ChunkGeneratorOverworld.java at `provideChunk`. This is where the chunk is generated. The X and Z values are chunk coordinates, which are determined by dividing the actual coordinates by 16 and flooring (rounding down) the result. By shifting X and Z forward by 12550821 / 16 and then shifting them back before the `chunk` variable is declared, we can shift the terrain so the far lands starts at 0,0.

The same may be done for ChunkGeneratorHell and ChunkGeneratorEnd in order to offset the terrain in the Nether and the End.

![MoveFL1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/MoveFL1.png)

![MoveFL2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/MoveFL2.png)

For the overworld, you should also mod populate(), in order allow the terrain features to generate properly. Note that some features (like ores) use both chunk coordinates and block coordinates, so you will see a subtle difference when comparing against the original terrain.

![MoveFL3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/MoveFL3.png)

![FLShift](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/FLShift.png)

Note that the terrain that would normally be spawn would now generate at (-12550821, -12550821).