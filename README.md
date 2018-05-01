# msx1logo

### Description

This is a proof of concept for displaying the MSX graphic logo on an MSX1 machine.

### Features

Doesn't do much, as of now. Just does what the description says.

### How to use

You just need the files in the [dist](https://github.com/mrparn/msx1logo/tree/master/dist) folder. From MSX-BASIC, type the following command:

`RUN "MSX1LBIN.BAS"`

You will see the graphic logo being drawn on the screen, and then it will wait for a key press. If you press a key, it will return to the MSX-BASIC prompt.

### Details

Every MSX2, MSX2+ and turboR machines have a nice graphic logo when you turn on the computer, but most MSX1 machines don't. I thought this was terribly unfair to the MSX1, so I set out to make a proof of concept for displaying the MSX graphic logo on MSX1 machines. I used the MSX2 boot logo and a vector MSX graphic logo as references for this project, but my version of the logo was actually carefully hand-drawn, pixel by pixel.

This was done because the MSX logo is actually a bit irregular, and since resolution and color limitations prevented me to use any antialiasing, it didn't look right at first, so I decided to redraw it, but taking extra care in making the jaggies as regular as possible. I also tried to make the logo look as close as possible to the MSX2 boot one, both in size and shape. I tried to make it fit in a grid, and you can find both the source PSD file (with the grid and layers) and a generated PNG file (with the TMS9918 palette) in the [prototype](https://github.com/mrparn/msx1logo/tree/master/prototype) folder.

I used this prototype as reference for the [generator](https://github.com/mrparn/msx1logo/tree/master/generator). In the folder you can find both a binary MSX-BASIC file and a plain text version for easy reading on a PC. I used this generator to create binary data that would be loaded by the final proof of concept.

In the final proof of concept, I load both the name and pattern tables, but generate the color tables in order to make it as small as possible in MSX-BASIC. I'm sure it's possible to make it even smaller if Assembly is used.

### Acknowledgements

I always thought about the MSX1 having a nice graphic intro, but never got around to work on it until I stumbled on [this forum post](https://www.msx.org/forum/msx-talk/general-discussion/msx1-boot-logo). Thanks to Manuel Bilderbeek for the inspiration and to NYYRIKKI for the info about the MSX2+ animated logo size.
