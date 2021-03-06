Saptapper
=========

Automated GSF ripper tool created by Caitsith2, revised by loveemu.
<https://github.com/loveemu/saptapper>

This modified version provides some extra options that might be useful.

Caitsith2's original version can be found at GSF Central
<http://www.caitsith2.com/gsf/ripping.html>

Downloads
---------

- [Latest release](https://github.com/loveemu/saptapper/releases/latest)

Usage
-----

Syntax: `saptapper (options) [GBA Files]`

### Options

`--help`
  : Show help

`-q, --quiet`
  : Do not output ripping info to STDOUT

`-r`
  : Output uncompressed GBA ROM

`-n [count]`
  : Set minigsf count

`-fd, --gsf-driver-file [driver.bin] [0xXXXX] [arm|thumb] [start|main]`
  : Specify relocatable GSF driver block and minigsf offset

`-od, --offset-gsf-driver [0xXXXXXXXX]`
  : Specify the offset of GSF driver block

`-os, --offset-selectsong [0xXXXXXXXX]`
  : Specify the offset of sappy_selectsong function

`-ot, --offset-songtable [0xXXXXXXXX]`
  : Specify the offset of song table (well known Sappy offset)

`-om, --offset-main [0xXXXXXXXX]`
  : Specify the offset of sappy_main function

`-oi, --offset-init [0xXXXXXXXX]`
  : Specify the offset of sappy_init function

`-ov, --offset-vsync [0xXXXXXXXX]`
  : Specify the offset of sappy_vsync function

`--tag-gsfby [name]`
  : Specify the nickname of GSF ripper

`--find-freespace [ROM.gba] [size]`
  : Find free space and quit

`--rom2gsf [GBA ROM file] [-m]`
  : Convert GBA ROM into GSF (-m for multiboot ROM)

`--minigsf [basename] [offset] [size] [count]`
  : Create minigsf files

Note
----

Most of the games using the sappy driver are ripped completely and automatically with
this program. The only manual step left, is sorting and optimizing the set.

If saptapper was unable to rip the game properly, but did find one of the sappy driver
functions identifying it as being sappy compatible, an error will be written to STDERR,
identifying what function it was not able to find.

Before submitting a gsf set that has been ripped, with or without saptapper, please at the 
minimum optimize the set first.  Ideally, all sfxs/voices should be removed, all 
music/jingles kept.
