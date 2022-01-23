To start off, decompile 1.12.2 with ModCoderPack. Instructions can be found online.

Once you're finished, it's time to unpatch the fix that removed the far lands. Navigate to net/minecraft/world/gen/NoiseGeneratorOctaves.java at the method `generateNoiseOctaves` and comment out or delete the two lines that end with `% 16777216L`. After this, the far lands will be back.

![FarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/FarLands.png)

![CornerFar](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/CornerFar.png)

![FartherLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/FartherLands.png)

Note: There is a crash when you load chunks between 2^26 and 2^27 blocks away. Here's an explanation: https://www.reddit.com/r/Minecraft/comments/9u9d4i/floats_minecraft_and_the_far_lands/

If you want to fix this crash, go to net/minecraft/world/gen/feature/WorldGenMinable at `generate` and change f1 to a double. Also remove the casts to float there. Your code should look like this:

![FixOres](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/FixOres.png)

Additionally, here are the far lands in the Nether. The bedrock ceiling has been removed for visibility.

![NFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/NFarLands.png)

![NFartherLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/NFartherLands.png)

Here are the End far lands.

![EFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/EFarLands.png)

![EFartherLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/EFartherLands.png)

Now let's work on removing the world border. We need to force the chunks beyond 30 million to be solid, and also expand the border so we can go past it.

You'll need to do a search for 30 million and -30 million (search for 30000000), and replace all of these with Integer.MIN_VALUE or Integer.MAX_VALUE. Next, navigate to net/minecraft/world/border/WorldBorder.java. Change `startDiameter` to 4294967294D (twice the integer limit), and push `worldSize` to the integer limit. Then, do a search for 3.0E7 and 3.2E7 and replace them all with the integer limit. Lastly, search for 29999872, 29999999, and 2.9999999(E7) and replace those too. Now, all restrictions should be removed. Keep in mind that trying to join a multiplayer server after you've made these changes is a really bad idea.
