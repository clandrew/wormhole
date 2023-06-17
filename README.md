# wormhole
This is a color-cycling demo for C256 and F256 Foenix computers.

Do you remember DirectDraw? The DirectX 5 SDK disc came with a bunch of samples, including one called "Wormhole". 

This is a port of that sample. Some details are described more [in this blog post](http://cml-a.com/content/). It's similar to the 'img' demo posted [here](https://github.com/clandrew/fnxapp/), except the palette is updated every frame.

Like the 'img' sample, you'll find there are two versions: a C256-based Vicky II one and an F256-based TinyVicky one.

How to use the TinyVicky 'bin' version:
  * Use an F256 system with a 65816-based CPU.
  * Build the vcproj accordingly.
  * Use a tool like the 'F256 Uploader', distributed by the hardware vendor, or FoenixMgr available [here](https://github.com/pweingar/FoenixMgr) to transmit the binary over COM3 (USB) interface. Choose "Boot from RAM" and load it at 0x800.

![alt text](https://raw.githubusercontent.com/clandrew/wormhole/main/Images/wormhole.PNG?raw=true)

-----
## Release

There are three built versions of the demo you can choose from
* A .PGZ executable for C256 Foenix
* A .BIN, for F256 Foenix, loaded at address 0800
* A .HEX, for F256 Foenix, compatible with [new support I added for 816-based f256](https://github.com/clandrew/fnxide/commit/c7dc6c1a05816ec8739ab344b915de85b0d9069d) in FoenixIDE

See the [Releases](https://github.com/clandrew/wormhole/releases) page to download.

-----
## Earlier Versions

Earlier versions of this demo were posted to the [fnxapp](https://github.com/clandrew/fnxapp/) repo, with a full commit history there. Eventually, the demo out-grew that repository and being shared with so many other things, so it was pulled out and moved into its own separate repository here.

-----

## Build

This demo is set up using Visual Studio 2019 which calls [64tass](https://tass64.sourceforge.net) assembler.

There are Visual Studio custom build steps which call into [64tass](https://tass64.sourceforge.net). You may need to update these build steps to point to wherever the 64tass executable lives on your machine. If there is an error when assembling, the message pointing to the line number gets conveniently reported through to the IDE that way.

For a best experience, consider using [this Visual Studio extension](https://github.com/clandrew/vscolorize65c816) for 65c816-based syntax highlighting.


