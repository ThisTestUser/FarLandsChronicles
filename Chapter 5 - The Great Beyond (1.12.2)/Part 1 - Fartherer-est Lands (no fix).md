With the far lands re-enabled, the fartherer/est lands do not seem to exist at all (vanilla) or seems to exist as a "jump" in the terrain (Forge).

For example, here is X/Z = +4312430307758379832:

![FarLandsW1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsW1.png)

(The terrain generates completely flat, and the holes are the result of sand falling.)

Here is the terrain at X=10004065811,Z=1004065811 (the X coordinate is at 10 billion, while the Z coordinate is at 1 billion)

![FarLandsW2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsW2.png)

It seems that when trying to generate the fartherer lands (by modifying the coordinate scale to 2939527156989.952) in Forge (with my 1.12.2 far lands mod), a "jump" in the terrain occurs at the normal start of the far lands. Note that the location of this phenomenon can be changed by adjusting the coordinate scale.

![FarLandsForge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsForge.png)

The terrain then "drops" back at a further distance (note: different seed here). The drop back happens at different coordinates and is dependent on seed.

![FarLandsDropBackForge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsDropBackForge.png)

At the start of the farther lands, the terrain of the seed 2666171903307131136 drops down instead of up. Whether or not the terrain is drops or rises depends on the seed itself.

![FartherDropForge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FartherDropForge.png)

However, opening the seed in vanilla (with the far lands re-enabled of course) results in the terrain being completely flat. This is the same seed as the image with the jump, 2666171903307131136):

![FarLandsFlat](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch5/FarLandsFlat.png)
