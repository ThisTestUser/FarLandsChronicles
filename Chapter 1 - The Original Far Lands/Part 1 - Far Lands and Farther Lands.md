Before we start, let's remove the jitter from the far lands. Follow the instructions in this video: https://www.youtube.com/watch?v=KGPwPC7u03w

Basically, you go to RenderList.java and delete all the float casts.

Now let's explore the far lands. Teleport to the far lands and we'll check out what's there.

![FarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/FarLands.png)

![FartherLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/FartherLands.png)

You can modify where the far lands and the farther lands start at ChunkProviderGenerate.java. Here's the function:

![NoiseGenerator](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/NoiseGenerator.png)

The 3 fields (double[]) that are obtained by running generateNoiseOctaves determine where the far lands start. The first field is the selector noise, whose overflow will mark the start of the farther lands. The second and third fields will overflow at X/Z += 12,550,821, marking the start of the far lands. We'll only look at double d for now, as double d1 can bring in the sky far lands (more on that later).

When the selector noise overflows before the far lands appear, this will happen:

![Selector](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/Selector.png)

Now, if you want to see what normal terrain looks like, removing the far lands is also possible. Decompile beta 1.8.1 with MCP and replace `generateNoiseOctaves` from NoiseGeneratorOctaves.java and `func_805_a` in NoiseGeneratorPerlin.java with the beta 1.8.1 code and the far lands will be gone.

Now, you might also want to remove the fake chunks. The boundary was set intentionally so that players wouldn't go past this point, but it is simple to remove. Do a search for `0xfe17b800` and `0x1e84800` (which represent 32 million and negative 32 million, respectively), and replace them with `Integer.MAX_VALUE` and `Integer.MIN_VALUE`. After replacing the 11 instances where this appears, the fake chunks are now gone. Trees and mobs will now generate all the way to the 32-bit integer limit, and if you look at the image of the farther lands, you'll see this happening.
