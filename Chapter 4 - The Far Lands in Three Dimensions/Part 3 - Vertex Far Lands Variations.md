The vertex far lands contain some of the most interesting terrain that can be generated. Here are the types of terrain I've encountered. Note that in one corner, more than one type of terrain can be seen.

* Floating Islands - This is probably what one would expect to be generated. Here, large floating islands can be observed, and it stretches on forever
* Solid - A solid wall of stone, along with some ores and caves generate.
* Empty - Nothing generates. In the void far lands, it is instead filled with water.
* Sky Far Lands - Sometimes, the vertex far lands are overriden and the sky far lands replaces them instead.
* Rectangular - The floating islands generate, but they seem more cubic than usual. This appears when transitioning between one of the phases above to another phase. Despite this, it appears that they can also be seen right before the farther lands start.

The farther lands also generate, although they don't have to. When the terrain right before the farther lands (1004065811, 2008131622, 1004065811) is floating islands, rectangular, or sky far lands, they will generate. When the terrain is solid or empty, they could generate, but there is a chance they don't.

Sometimes, the terrain "recedes". In this case, there isn't anything right before the vertex farther lands.

Areas not in the vertex far lands region (abs(X and Z) > 12550821, abs(Y) > 25101642) will always generate what you expect them to generate.