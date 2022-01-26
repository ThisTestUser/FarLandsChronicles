First, we will use 196106.574487 for the Y-scale (more details in Part 0). This allows for the sky far lands to appear at height 128. Like the other far lands, the terrain appears blocky.

Seed for all images (except where noted): 3192545518397860029

![17SkyFar](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SkyFar.png)

Here is the terrain right before the vertex far lands, the intersection of 3 different types of far lands.

![17SkyIntersect](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SkyIntersect.png)

Below is the corner far lands (before intersecting with the sky far lands).

![17FarStack](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FarStack.png)

And below is the vertex far lands. Because the terrain has been flattened, it is harder to tell the difference between the corner and vertex far lands, but it does look like that the terrain becomes more chaotic in the vertex far lands.

![17FarVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FarVertex1.png)

Like the vertex far lands in Cubic Chunks, there are many variations possible. For example, this variant of the vertex far lands is entirely soild terrain.

![17FarVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FarVertex2.png)

In the vertex farther lands (Y above 128), the terrain can generate completely soild or empty.

![17FartherVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVertex1.png)

![17FartherVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVertex2.png)

In another seed though, even more variations can be found. This is the same seed as the receding far lands shown in the 3D far lands chapter.

![17FartherVertexAlt1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVertexAlt1.png)

![17FartherVertexAlt2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVertexAlt2.png)

Now let's look at the void far lands. Set the Y-scale to 784426.297949, and the void far lands will start below Y=-32.

![17VoidFar](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidFar.png)

As we approach the intersection, the void far lands mix in with the other types of far lands, and like the corner far lands, intersect with aquifers.

![17VoidIntersect](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidIntersect.png)

![17FarVoidVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FarVoidVertex1.png)

![17FarVoidVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FarVoidVertex2.png)

Below, the edge far lands blend with the sky far lands. It is harder to tell the difference between the two, as the sky edge far lands occupy only a narrow edge.

![17VoidEdge](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidEdge.png)

As we move into the farther lands, it becomes hard to draw a conclusion as to what the terrain is doing. Here, the vertex void farther lands appear to be generating terrain below Y=-32.

![17FartherVoidVertex1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertex1.png)

From the below pictures, it seems like stretching the Y-scale changes the terrain generation underground (remember this is the same seed and same location as the image showing the ocean a slab of deepslate in the previous part).

![17FartherVoidVertex2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertex2.png)
 
![17FartherVoidVertex3](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertex3.png)

![17FartherVoidVertex4](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertex4.png)

![17FartherVoidVertex5](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertex5.png)

In another axis, there is a soild wall of terrain below Y=-32, even before the farther lands are reached.

![17FartherVoidVertexOther](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17FartherVoidVertexOther.png)

Now, we set the Y-scale to 62754103.8359. This allows the Y-dimension farther lands to start at Y=64 (not Y=32 as expected), and causes the sky far lands to completely replace normal terrain.

![17SpawnFarther1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SpawnFarther1.png)

![17SpawnFarther2](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SpawnFarther2.png)

When the normal far lands start to generate, the 3 different types of far lands mix.

![17VoidVertex](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidVertex.png)

The sky farther lands start at Y=64, as shown below.

![17SkyVertex](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SkyVertex.png)

In the farther lands, the terrain generates nothing (the water is due to the aquifer fix). Note that it could also generate completely filled with stone except for below sea level.

![17VoidFarther](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidFarther.png)

Here is another axis of the far lands. At (-1 billion, 1 billion), the terrain is completely soild. The terrain below shows the transition from the normal vertex far lands to soild terrain. This behavior is also seen in the 3D far lands exploration.

![17SkyTransition](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17SkyTransition.png)

What's more interesting is that the blocky deepslate generated in void far lands also fades out into endless ocean. This appears to be happen even when the Y-scale isn't stretched.

![17VoidTransition](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch6/17VoidTransition.png)
