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
