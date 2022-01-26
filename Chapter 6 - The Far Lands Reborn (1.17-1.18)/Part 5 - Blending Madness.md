In 1.18, there exists a feature called blending, where old terrain is blended with the new terrain to prevent obvious chunk borders. This works by attaching to the top block and gradually adjusting the height until it reaches the height of the newly generated terrain.

So how does this work with the far lands?

images

As the top of the far lands (Y=255) is made of grass, the chunks that generate right next to the old chunks will start at max height, and then ramp down until it reaches the natural generated height.

But what happens when the surface is not dirt, but some unnatural block? Note that this was done using a modded version of 1.12, as a modded world wouldn't have blending applied.

images

Here, it looks like the blender attaches to the stone instead, and then ramps down from there.

When the stone is replaced, the blender still tries to find stone blocks to attach to. Sometimes it ends up blending successfully, sometimes it only puts a lid on the terrain, and sometimes it fails completely.

images