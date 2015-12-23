NINJAMCast
Includes WDL Framework, ready to compile on Ubuntu 14.04

24/07/2011

Hello,
this works and compiles on Ubuntu Ubuntu 10.04.3 LTS 64bits
Didn't test on other systems.

All kudos to Cockos, and particularly Justin, Brennan and All ppl who
contributed to do this.

I just did a workable makefile, and modified some variables in the
njclient.cpp file.

You'll need the following libs and packages installed for it to compile correctly:

gcc-4.3-multilib
lib32ncurses5 
lib32ncurses5-dev
libasound2
libasound2-dev
libvorbis
libvorbis0a
libvorbisenc2
lib ogg 
lib mp3lame


I may have forgot some packages, check the errors and fix it.


To compile ninjamcast go to ninjam/ninjamcast and then type make.
Ignore the warnings.
Then do read the example cfg and set it up.

Have fun.

DaMNeD
