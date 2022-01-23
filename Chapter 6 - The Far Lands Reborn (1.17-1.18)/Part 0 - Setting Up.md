To explore the far lands in 1.17.1, we will need the official Caves & Cliffs datapack, along with my far lands mod. Without the datapack, the far lands are the same as in previous versions.

To get the Y-axis far lands to appear, it is necesary to increase the height scale in the Y-direction. The way that this is done is by modding the C&C datapack. Head inside the datapack ZIP and navigate to data/minecraft/worldgen/noise_settings/overworld.json and extract it. Find "y_scale" inside the JSON file. The y coordinate where the Y-axis far lands (both sky and void) start can be calculated by dividing 25,101,642 by that scale (the scale is very close to 1 and can be treated as such).

If you've raised the scale to a high enough number and you have my far lands mod active, you will see the sky/void far lands.

For 1.18.1, only the far lands mod is needed, as the new terrain features are included in vanilla.

For the Y-axis far lands to appear in 1.18, the height scale needs to be raised there. First, create a normal world, and then exit to the main menu. Select the world again, press "Edit", and press "Export World Generation Settings". The exported JSON will appear in the world folder in saves.

After this, head over to https://misode.github.io/worldgen/noise-settings/ and use the presets button to select the overworld preset for 1.18. Press the download button on the bottom right to download the preset as a JSON. Ensure that your preset file is over 4,500 lines long.

Now go back to the exported worldgen settings, highlight ```"minecraft:overworld"``` in the line starting with ```"settings": "minecraft:overworld"```. Replace that with the entire overworld noise preset (copy and paste it in).

Find ```y_scale``` in the file. You can increase the scale to make the sky/void far lands appear, as dividing 25,101,642 by that scale gives the start of the vertical far lands. Like 1.17, this requires my far lands mod to be enabled.