The vertex far lands contain some of the most interesting terrain found in vanilla Minecraft. Before we head into the vertex farther lands, let's recap the types of terrain seen so far.

* Normal - This refers to the amplified-like terrain found in the vertex far lands.
* Normal Farther Lands - This refers to the non-vertex farther lands that are unaffected by distortions.
* Blocky - This is the blocky version of the amplified (normal) variant.
* Blocky Farther Lands - This is the farther lands but distorted by the blockiness unique to the vertex far lands.
* Solid - Stone generates everywhere. Caves and ores are carved through this terrain. No difference can be found if we cross the farther lands boundary.
* Empty - Nothing generates at all but air. In the void far lands, the air is replaced with water. No difference can be found if we cross the farther lands boundary.

The blocky variant is a distortion of the normal amplified terrain. There are varying degrees to this blockiness. In the vertex far lands, the more blocky it is, the more sharp corners it will have. At first, the terrain generator will attempt to round the corners, but as the blockiness increases the terrain resembles cubes of various sizes joined together.

For the edge farther lands (including sky), the blockiness causes the terrain to generate sharp corners and thin rectangular planes. In the corner farther lands, the stacks are often one block high.

Blocky terrain serves as an intermediate state between solid/empty and normal. Before normal terrain can transition to solid or empty, it must gradually become distorted, and then when the distortion is at a maximum the transition can occur across a plane. The only exception is when two transitions intersect, where the terrain at the intersection point is normal.

Transitions reflect a change from one type of terrain to another. They can be parallel to one axis or parallel to none. There are two types of transitions possible, blocky and solid, and blocky and empty. Note that transitions are possible in both directions.

Transitions are continuous across different corners of the vertex far lands. This is the most obvious with transitions parallel to an axis, where flipping the sign of the X or Z coordinate reveals another transition.

Multiple transitions are possible within one corner. In the seed mentioned in part 1, two transitions can be found in the ++ axis. A transition to solid can be seen in the seventh image (the hard boundary), and a transition back to blocky is visible in the second to last image. Transitions can also intersect, which can be seen in the void far lands images.

Areas not in the vertex far lands region (abs(X and Z) < 12550821 and abs(Y) < 25101642) are not affected by distortions or transitions to solid or empty.

It's time now to head into the vertex farther lands, or when the selector noise overflows on all 3 axises.

If the terrain is entirely solid or empty just before, no difference can be seen past the vertex farther lands. However, if there is normal or blocky terrain just before, the vertex farther lands usually manifests as a region of solid or empty terrain.

![SVFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther1.png)

![VVFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther1.png)

If limited to the farther lands, the region of solid or empty terrain remains confined to it. It is still affected by transitions extending all across the vertex far lands.

![SVFartherT1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFartherT1.png)

![VVFartherT1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFartherT1.png)

It is possible to find interesting terrain in the vertex farther lands though. Below shows one example, from seed -936504578442456880.

![SVFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther2.png)

![SVFarther3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther3.png)

The repetitive like terrain does not last forever. A peak can be seen nearby, and the terrain starts losing elevation from there. No other terrain can be found in this corner.

![SVFarther4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther4.png)

Another example of interesting terrain is below. The terrain is attached to the side instead of the bottom.

![SVFarther5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther5.png)

Note that the terrain just below is part of the corner farther lands. It suggests that selector noise overflow on the Y axis amplifies the terrain.

![SVFarther6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther6.png)

Unlike before, this terrain seems to go on forever. This is also true going upwards as well, although the integer limit quickly cuts off our view.

![SVFarther7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther7.png)

To view the effects of a transition on this terrain, we must double the noise scales to make the far and farther lands start twice as close. After doing this, we can see the same type of distortion that we have seen in the vertex far lands, followed by the transition.

![SVFartherT2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFartherT2.png)

Here are examples of interesting terrain generating in the void farther lands.

![VVFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther2.png)

![VVFarther3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther3.png)

![VVFarther4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther4.png)

In the below example, a wall of stone is generated that moves closer when traveling down. As a result, it quickly merges with the vertex farther lands boundary.

![VVFarther5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther5.png)

Blockiness can be seen as we move closer to a transition. The following three images shows how the terrain changes as blockiness is applied.

![VVFarther6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther6.png)

For the below two images we need to scale up the noise by three to bring the transition within the integer limit.

![VVFarther7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther7.png)

![VVFartherT2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFartherT2.png)

By searching even more seeds, another type of terrain appears to generate. The corner starts as a repeating pattern like we've seen before.

![SVFarther8](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther8.png)

Moving forward reveals a new type of terrain trying to emerge from it. This terrain has more variety than the repeating terrain shown previously.

![SVFarther9](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther9.png)

![SVFarther10](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther10.png)

![SVFarther11](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther11.png)

Eventually, the new terrain takes over completely. From the +X side it first starts with egg-like holes, before transitioning briefly to chaotic terrain and finally fading to air.

![SVFarther12](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther12.png)

![SVFarther13](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther13.png)

Moving up the Y axis also results in chaotic terrain taking over. Again, egg-like holes start generating, followed by chaotic terrain before becoming sparse and fading to air.

![SVFarther14](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther14.png)

![SVFarther15](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther15.png)

![SVFarther16](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther16.png)

If we move forward in the X and Z axises, the fade to air does not happen. Instead, there is a transition from sparse to chaotic terrain when moving up the Y axis. The repeating terrain seen before does not extend to this point.

![SVFarther17](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther17.png)

In the -+ axis, the chaotic terrain manifests differently. In the +Z direction, there is a transition from egg-like structures (the opposite of the holes seen before) to chaotic terrain.

![SVFarther18](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther18.png)

![SVFarther19](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther19.png)

It is clear from the below image that the terrain is the inverse of the ++ axis. Notice how rectangular holes form instead of lines.

![SVFarther20](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther20.png)

The chaotic vertex farther lands are affected by distortions and transitions. Below shows the distortion being applied to the egg-like holes.

![SVFarther21](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFarther21.png)

Just before a transition, the terrain is extremely rectangular. Similar terrain can be found in the vertex far lands when the noise scales are increased by a large ratio.

![SVFartherT3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/SVFartherT3.png)

From the same seed as all the images before, we can also find chaotic terrain in the void farther lands.

![VVFarther8](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther8.png)

![VVFarther9](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther9.png)

![VVFarther10](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther10.png)

Here is the terrain just before a transition in the void farther lands.

![VVFartherT3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFartherT3.png)

Here is a repeating pattern, similar to what we saw in the sky farther lands, intersecting with chaotic terrain. Note how quickly the chaotic terrain manifests compared to the sky farther lands.

![VVFarther11](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther11.png)

The below two images show a quick transition from egg-like holes to chaotic terrain. For this seed, we encounter chaotic terrain in the void farther lands much earlier.

![VVFarther12](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther12.png)

![VVFarther13](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch4/VVFarther13.png)
