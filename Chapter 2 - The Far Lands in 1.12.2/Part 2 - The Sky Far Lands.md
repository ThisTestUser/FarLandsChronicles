The sky far lands are what generates when the octaves overflow in the Y-direction. When d1 in ChunkProviderGenerate.java is multiplied by 2^18, they start at about Y=84.

![SkyFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SkyFarLands.png)

![SkyFarLandsStack](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SkyFarLandsStack.png)

When the selector noise for Y axis overflows first, we see floating islands and also "spiky" terrain, which is similar to what we saw back in beta 1.7.3. I multiplied the selector noise by 2^30 in this case, instead of 2^25 before.

![SelectorOverflow](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/SelectorOverflow.png)

The sky far lands also exist in the Nether and the End, and they can be added in by modifying ChunkProviderHell.java and ChunkProviderEnd.java, respectively.

![NSkyFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/NSkyFarLands.png)

![NSkyStackLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/NSkyStackLands.png)

![ESkyFarLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/ESkyFarLands.png)

![ESkyFarLands1](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/ESkyFarLands1.png)

![ESkyStackLands](https://raw.githubusercontent.com/ThisTestUser/FarLandsChronicles/master/assets/Ch2/ESkyStackLands.png)