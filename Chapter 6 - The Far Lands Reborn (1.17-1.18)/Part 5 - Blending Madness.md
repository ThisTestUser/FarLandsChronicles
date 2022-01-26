In 1.18, there exists a feature called blending, where old terrain is blended with the new terrain to prevent obvious chunk borders. This works by attaching to the top block and gradually adjusting the height until it reaches the height of the newly generated terrain.

So how does this work with the far lands?

![BlendFL1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL1.png)

![BlendFL2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL2.png)

As the top of the far lands (Y=255) is made of grass, the chunks that generate right next to the old chunks will start at max height, and then ramp down until it reaches the natural generated height.

There is also some limited blending of air pockets inside, where the blender generates some air blocks to prevent abrupt edges.

![BlendFL3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL3.png)

But what happens when the surface is not dirt, but some unnatural block? Note that this was done using a MCP-modded version of 1.12, as a modded world wouldn't have blending applied.

![BlendFL4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL4.png)

Here, it looks like the blender attaches to the stone instead, and then ramps down from there.

When the stone is replaced, the blender still tries to find stone blocks to attach to. Sometimes it ends up blending successfully, sometimes it only puts a lid on the terrain, and sometimes it leaves the surface exposed completely.

![BlendFL5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL5.png)

![BlendFL6](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL6.png)

When dealing with non-far lands terrain, the blender is more successful at connecting the edges.

![BlendFL7](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/BlendFL7.png)
