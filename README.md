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

### Frome PB Metlako (thread)[https://www.diyaudio.com/community/threads/metlako-a-small-affordable-two-way-unity-waveguide.342019/page-3] 
Utilised ideas from MTM design where the dispertion at a freq is controlled by the distance between drivers
```
For example, if you have two midrange taps seperated by five inches, they'll generate a beamwidth of about 70 degrees at 1,350Hz. Here's the math:

speed of sound / distance / 2 =

13500 / 5" / 2 =

1,350Hz
```
This only gives us 70deg, need to lookup some better maths/explanation for this. :)

### frequenmcy / wavelength table

#### high frequncies

|temp(c) mm | 1k  | 1.25k | 1.6k | 2k  | 2.5k | 3.15k |
|-----------|-----|-------|------|-----|------|-------|
| 20C - 1   | 343 | 274   | 214  | 172 | 137  | 109   |
| 20C - 1/2 | 172 | 137   | 107  | 86  | 69   | 55    |
| 20C - 1/4 | 86  | 69    | 54   | 43  | 34   | 27    |


#### mid frequencies

|temp(c) mm | 400hz | 500hz | 630hz | 800hz |
|-----------|-------|-------|-------|-------|
| 20C - 1   | 858   | 686   | 544   | 429   |
| 20C - 1/2 | 429   | 343   | 272   | 215   |
| 20C - 1/4 | 215   | 172   | 136   | 107   |

## TODO:


## Issues:

1. using ATH 4.7 as I did not get a STL output from 4.8 (still not getting stl from 4.8 but can import into fusion360 - have tried an older version of gmsh)
    1. Able to ge a responbse  Update I am still a noob but can get an output after processingf the msh as per [[https://www.youtube.com/watch?v=I5dvgBgtbos&t=467s]
        - [https://www.diyaudio.com/community/threads/akabak-3.353871/]
        - [https://www.youtube.com/watch?v=-IYF8awp_fA&lc=UgwxIxbMf6nDCn-kpNZ4AaABAg]
        - [https://www.avsforum.com/threads/akabak-for-dummies.1258118/]
        - Old ABEC is also available and will work with the scripts no problems.
    2. to get ath and abec working
        1. download ath 4.8 and the pre release 4.9 - copy 4.9 into 4.8 ( 2 files) 1 is ath.exe and thew other ius a script (replace original)
        2. gmesh 4.11 works
        3. after you wun ath you will need toopen the .msh file in gmesh and export saving as version 2 ASCII, rename this to the origianl .msh file name.  
        4. Project shoulld now open in ABEC 3 no problems... 

1. Unsure of where to start for the actual Mid entry horn
    1. modelling issues    
        - need to model a unity in Akabak / ABEC
        - some old scripts here [https://www.diyaudio.com/community/threads/unity-horn-script-for-akabak.109568/] but they do not appear to work and/or i cannot import them properly. many errors and no image in bem 