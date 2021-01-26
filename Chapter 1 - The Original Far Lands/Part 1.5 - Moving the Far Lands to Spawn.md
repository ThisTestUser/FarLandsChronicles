There's a bug in beta 1.7.3 where at every power of 2 past 2^19, some chunks from spawn will be ported all the way out to said distance. Notably, this still works for 2^24, which is in the far lands, and powers of two 2^25 and above, which are beyond the 32 million fake chunk boundary. This is the only instance where terrain features such as trees and ore veins can generate past 3.2E7 (without patching the fake chunks).

For example, when the x-axis and the z-axis are both equal to 2^25, the far lands give away to the terrain seen at spawn.

This bug seems unrelated to the far lands themselves, as editing the far lands out (by stopping the overflow) did not fix this issue.

![NormalTerrainNoFL](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/NormalTerrainNoFL.png)

However, this bug can create some interesting effects. Here's a typical spawn.

![Spawn](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/Spawn.png)

And now, we teleport to 2^25 in both axes, and we see the spawn showing up here.

![SpawnInFL](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/SpawnInFL.png)

After exploring the whole area, we teleport back to spawn. Something interesting shows up; the far lands are ported to spawn!

![FLInSpawn](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/FLInSpawn.png)

Now, let's quickly modify the terrain with an explosion.

![ExplodeSpawn](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/ExplodeSpawn.png)

When we go back to 2^25, we see that the explosion has carved out a hole, even in the "unmodifiable" far lands.

![ExplodeFL](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch1/ExplodeFL.png)

This issue is unrelated to the far lands or the fake chunks, and it no longer exists in modern versions.
