We're about to see what the Far Lands looks like, modded. Here are the mods we are using:

* aether_legacy-1.12.2-v1.4.4
* Atum-1.12.2-2.0.16
* Erebus-1.0.31
* TheBetweenlands-3.5.5-2573-SNAPSHOT-universal (Warning: You must use a snapshot version)
* AbyssalCraft-1.12.2-1.9.15
* GalacticraftCore-1.12.2-4.0.2.238, Galacticraft-Planets-1.12.2-4.0.2.238, MicdoodleCore-1.12.2-4.0.2.238
* twilightforest-1.12.2-3.10.1013-universal

Note: The GalacticCraft addons present are ExtraPlanets-1.12.2-0.5.8 and More-Planets-1.12.2-2.0.22-GC238.

These mods were not designed to work in the far lands, and some of them have to be modded. We will be using JByteMod and Recaf to add in try-catch blocks or delete instructions.

For AbyssalCraft, we'll need to add a try-catch loop at com/shinoow/abyssalcraft/common/world/gen/WorldGenDreadlandsStalagmite.java in generate(). Go into JByteMod and navigate to the method, and then add 3 instructions at the end. You can duplicate the FrameNode before and then start editing the contents inside. Just make sure your code looks like this:

![AbyssalCraftMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/AbyssalCraftMod.png)

Next, add a try-catch block. The end and handler labels should match the one you see in the image before.

![AbyssalCraftMod1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/AbyssalCraftMod1.png)

After you've saved the modded JAR, delete SHINOOW.RSA and MANIFEST.MF from the META-INF. This will allow the mod to run while modified.

For Erebus, navigate to erebus/world/biomes/decorators/BiomeDecoratorBaseErebus.java and change an athrow to a pop in decorate().

![ErebusMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/ErebusMod.png)

For The BetweenLands, you must grab a snapshot version, because the main version has a hash check. Navigate to thebetweenlands/common/world/gen/feature/structure/WorldGenCragrockTower.java, in the method tower(). Add an exception handler at the bottom (3 instructions):

![TheBetweenlandsMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/TheBetweenlandsMod.png)

Now, open up Recaf and navigate to the method. Open the try-catches, and add an exception named "java/lang/NullPointerException". The end and handler labels should be the second to last and last labels, respectively. Save, and you should be done.

![TheBetweenlandsMod1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/TheBetweenlandsMod1.png)

For the GalacticCraft core mod, you need to change an athrow to a pop at micdoodle8\mods\galacticraft\api\prefab\world\gen\BiomeDecoratorSpace.java decorate().

![GalCraftMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/GalCraftMod.png)

For ExtraPlanets, you need to replace an athrow with a pop, at com\mjr\extraplanets\planets\Jupiter\worldgen\BiomeDecoratorJupiterOther.java func_180292_a().

![ExtraPlanetsMod](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch3/ExtraPlanetsMod.png)