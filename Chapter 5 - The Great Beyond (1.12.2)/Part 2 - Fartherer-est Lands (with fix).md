A long time ago, it was assumed that the far lands were completely fixed in beta 1.8, with no new sets of far lands appearing, no matter how far you go. Well, some have then tried to adjust the coordinate noise to a very high number (2939527156989.952 will result in the fartherer lands appearing at 12550821), and they have found that the far lands do generate, even in vanilla (with the overflow fix).

(Important Note: You must disable the overflow by adding back the `% 16777216L`. If this is not done, there will be no new sets of far lands.)

Here are the far lands in vanilla. X/Z = +53905379859335561:

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