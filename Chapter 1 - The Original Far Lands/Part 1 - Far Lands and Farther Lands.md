Before we start, it's probably a good idea to patch out two undesirable float bugs that will hinder exploration of the Far Lands: the "offset"/"jitter" bug and the issue with sand/gravel entities constantly falling and generating thousands of items.

To get rid of the jitter issue, we'll need to navigate to RenderList.java and remove some float casts, as well as convert floats to doubles accordingly. On lines 11, 12 and 13, change the declared floats to doubles. Delete the three float casts on lines 24, 25 and 26, and delete the float cases from line 50 as well as changing "glTranslatef" to "glTranslated". This should completely get rid of the jitter issue. See this video for more info: https://www.youtube.com/watch?v=KGPwPC7u03w

To fix sand and gravel, go to BlockSand.java. On line 28, we need to delete the float casts, and change each instance of "0.5F" on that line to "0.5D". Once this is done, sand and gravel should now fall correctly and we won't be forced to constantly use the "killall" command every few minutes.

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
