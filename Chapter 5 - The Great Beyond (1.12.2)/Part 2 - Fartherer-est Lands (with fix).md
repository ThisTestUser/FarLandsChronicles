A long time ago, it was assumed that the far lands were completely fixed in beta 1.8, with no new sets of far lands appearing, no matter how far you go. Well, some have then tried to adjust the coordinate noise to a very high number (2939527156989.952 will result in the fartherer lands appearing at 12550821), and they have found that the far lands do generate, even in vanilla (with the overflow fix).

(Important Note: You must disable the overflow by adding back the `% 16777216L`. If this is not done, there will be no new sets of far lands.)

The far lands can be brought back in vanilla by simply adjusting the coordinate scale. Even at low coordinate scales, a new type of far lands appears. The appearance of this kind of far lands depends on the coordinate scale, so it is presumed to not happen when offsetting.

(Caution: There may be a StackOverflowError as a result of liquids flowing. Go to BlockStaticLiquid, at updateLiquid() and insert a return statement if the current stacktrace is over 200 entries long.)

The below image is with a coordinate scale of 532952700. The two images below used a seed of 874167528226366678.

![CoordScaleFL1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFL1.png)

This image used a coordinate scale of 533952700.

![CoordScaleFL2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFL2.png)

A coordinate scale of 538952700 would result in the normal terrain being only one chunk wide, and even higher coordinate scales would make the far lands appear everywhere. It is important to note that the far lands that will appear in offsetting later also show up.

![CoordScaleFar1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFar1.png)

![CoordScaleFar2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFar2.png)

The above images were taken with a coordinate scale of 2939527156989.952. At the same coordinate scale, the farther lands generate at the expected position:

![CoordScaleFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFarther1.png)

![CoordScaleFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/CoordScaleFarther2.png)

Now lets see what the far lands look like with offsetting. Here are the far lands in vanilla. X/Z = +53905379859335561:

![FarLandsV1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsV1.png)

It seems that the terrain generator begins breaking down a bit before this. This does NOT happen when the far lands are "added back":

![FarLandsV2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsV2.png)

As we go deeper, the chunk errors begin to severely affect the far lands. X=1152921504606846976, Z=53905379859335561

![FarLandsErrorV1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsErrorV1.png)

The terrain generator then becomes even weirder (the two images were taken a couple hundred blocks away from each other):

![FarLandsErrorV2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsErrorV2.png)

![FarLandsErrorV3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsErrorV3.png)

Now, we approach the farthest lands, which in vanilla generates at X/Z = +4312430292602321672:

![FarthestLandsV](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarthestLandsV.png)

Chunk errors appear on both sides of the corner far lands. The edge far lands don't seem to be affected.

As we go even further, the corner far lands eventually becomes flat, while the edge far lands becomes long and continuous.

The far lands you see in the above images all generate as a result of the modulo fix breaking down. Starting from 1.14, both variants of the far lands (the one that appears when raising the coordinate scale and the one that appears at high coordinates) do not appear at all.