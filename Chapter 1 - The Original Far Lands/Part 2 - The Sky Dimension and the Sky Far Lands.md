Let's have a look at the sky far lands. Similar to how the giant wall generates when the octaves overflow, the wall can also generate in the Y direction. You can enable them by multiplying d1 in ChunkProviderGenerate.java at `func_4061_a` by 2^18.

![SkyFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/SkyFarLands.png)

When the sky far lands merge with the edge far lands, the vertex far lands start to appear.

![VertexFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/VertexFarLands.png)

![VertexFarLands1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/VertexFarLands1.png)

The sky farther lands also exist, but it's hard to tell here. If we force the selector noise to overflow first, we'll get floating islands:

![Floating](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/Floating.png)

Now, let's look at the sky dimension. The sky dimension is an unfinished dimension that was supposed to be the opposite of the Nether. It was removed eventually, but you can enable it at `getProviderForDimension` in WorldProvider.java by replacing WorldProviderSurface with WorldProviderSky.

Here's how the sky dimension looks:

![SkyDimension](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/SkyDimension.png)

And here's the far lands:

![SkyDimFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/SkyDimFarLands.png)

The sky dimension's sky far lands can be enabled in ChunkProviderSky.java, at `func_28073_a`. Here is what it looks like when intersected with the edge far lands:

 ![VertexSkyFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/VertexSkyFarLands.png)
 
 ![VertexSkyFarLands1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/VertexSkyFarLands1.png)
 
 When the selector noise overflows first, floating parts of the island are observed.
 
 ![FloatingSky](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/FloatingSky.png)
 
 Next time, we'll look at how the far lands appear in modern versions (1.12.2), after it is artificially re-enabled.