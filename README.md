# mt122_unity_conversion


## Info
Based upon a [MT122](https://www.speakerplans.com/index.php?id=mt122) open source design from Rog Mogale from speakerplans.com.

12" section will be removed and used for mids (1 per cab).
2" section will be replaced by a mid-top unity/synerge style horn utilising 1x B&C DE250 and 2x B&C 4NDF34.

Coverage angle will be 60x40.

## Design goals

Ideally the 4NDF34 covers 600/700 up to 1.5k-3.5k, DE250 to cover above.

Max width of the outside to match the MT122 (567mm) and the outside to have the same 10 degree angle or less. 

## Construction 

I have a Voron 2.4 with a max build size of 350L x 350W x 300H, ideally final construction is 3D printed for horn/waveguide on a plywood box, if required a 3d printed mould for the horn/waveguide then fibreglass/composite construction can be done.  

## Folder Structure

Folder structure guide

### Resources

A place to store resources for the project that are usefull beteen versions. I.E. A fusion 360 model of the B&C 4ndf34 with cone at XLIM to carve the minimum front cavity and and give an idea for physical placment. 

### Versions

Pretty self explanatiory, prototype versions aare the first run of new ideas. E.G. Proto_01 - DE250 horn for testing without the mid driver. 

## Ideas/guides for mid placement and ports
1. Close as possible for highest XO
    - driver tapped into horn/waveguide will play up to a frequency where the circumference of the cross sectional area of the tap is equal to one wavelength. (diy audio)[https://www.diyaudio.com/community/threads/please-critique-my-multi-entry-horn-simulation.332137/post-5655619]
    - The distance between the acoustical center of the compression driver and the tap point must be one half a wave length or less. (same link as above)
2.  Ideal placement
    - circumference is 1 wavelength of the highest freq
    - distance between accoustic centres of DC and mid driver is 1/2 wavelength of highest freq.
3. Smaller chamber/ throat for the mid raises the high rolloff
4. Diameter (starting point) can be 2x 17.4mm per driver, this is 1:12 compression ratio (sd=57/4,75cm²).

## TODO:


## Issues:

1. using ATH 4.7 as I did not get a STL output from 4.8
2. Unable to get respose chart from Akabak - I am a noob at this program
    - [https://www.diyaudio.com/community/threads/akabak-3.353871/]
    - [https://www.youtube.com/watch?v=-IYF8awp_fA&lc=UgwxIxbMf6nDCn-kpNZ4AaABAg]
    - [https://www.avsforum.com/threads/akabak-for-dummies.1258118/]
3. Unsure of where to start for