In order to explore the far lands in beta 1.7.3, we'll need to be able to edit Minecraft easily. The best way to do this is by decompiling the game using ModCoderPack. Here I'll be decompiling the JAR with Single Player Commands injected into it. This will cause some errors, but they're easy to fix.

First, download and install Single Player Commands. You can find a tutorial online. Next, download ModCoderPack for beta 1.7.3, and extract the contents into a folder.

Follow steps 1-3 here: https://gist.github.com/coffeenotfound/e4af949d32203574e0deadcbcb2385ce

Also, get the modded Minecraft JAR and place it in /jars/bin as minecraft.jar. Also find WorldEdit.jar inside the modded JAR and extract it in the folder.

In order for MCP to recognize WorldEdit.jar, we need to add it to the libraries list. Find mcp.cfg in the conf folder and search for ClassPathClient. Add the following to the end:

`,%(DirJars)s/bin/WorldEdit.jar`

Run decompile.bat. Everything should work out.

Now, there are still a few fixes to work out. Replace minecraft.jar with the unmodded version of beta 1.7.3. Launch your IDE (I'm using Eclipse) and add WorldEdit.jar as a library. After this, there shouldn't be any compiling errors. However, due to a bug in the decompiler, you'll need to fix some lines of code to run the program correctly.

First is SPCCommand.java. You should add `@Retention(RetentionPolicy.RUNTIME)` above where the class is declared, and also change the class into an interface, add default tags to the methods. When you're finished, the code should look like this:

![SPCCommand](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/SPCCommand.png)

Now navigate to beforeUpdate at PlayerHelper.java. Search for `vector.size()`, and add an `i++` at the end to make sure the loop continues. Delete the `i++` you see below. Here is what you end up with.

![PlayerHelper](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/PlayerHelper.png)

This should be it for the fixes.

