# wormhole
This is a color-cycling demo for C256 and F256 Foenix computers.

Do you remember DirectDraw? The DirectX 5 SDK disc came with a bunch of samples, including one called "Wormhole". 

This is a port of that sample. Some details are described more [in this blog post](http://cml-a.com/content/). It's similar to 'img', except the palette is updated every frame.

Like the 'img' sample, you'll find there are two versions: a C256-based Vicky II one and an F256-based TinyVicky one.

How to build and load the TinyVicky 'bin' version:
  * The build step uses [64tass](https://tass64.sourceforge.net) as usual. 
  * The build creates a .bin file, which is a raw dump of bytes to be patched in at an externally-chosen location.
  * Use a tool like the 'F256 Uploader', distributed by the hardware vendor, or FoenixMgr available [here](https://github.com/pweingar/FoenixMgr) to transmit the binary over COM3 (USB) interface. Choose "Boot from RAM" and load it at 0x800.

The F256 version of sample uses 65816-based code, and requires a 65816-based CPU.

![alt text](https://raw.githubusercontent.com/clandrew/fnxapp/main/Images/wormhole.PNG?raw=true)
