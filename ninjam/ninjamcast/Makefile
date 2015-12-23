#############################################################
# CPU optimization section
#############################################################

OPTFLAGS =  -O2 

ifdef MAC
OPTFLAGS += -D_MAC -mcpu=7450
LFLAGS = -framework coreaudio -lncurses.5 -lm
else
OPTFLAGS += -malign-double
#LFLAGS = -Wl,--no-as-needed -lncurses -lm -lasound
LFLAGS = -lncurses -lm -lasound -ldl
endif

#############################################################
# Basic Configuration
#############################################################

# we MUST have -fomit-frame-pointer and -lm, otherwise we hate life
CFLAGS = $(OPTFLAGS) -s
# CFLAGS += -Wshadow
CC=gcc
CXX=g++

OBJS += ../../WDL/jnetlib/asyncdns.o
OBJS += ../../WDL/jnetlib/connection.o
OBJS += ../../WDL/jnetlib/listen.o
OBJS += ../../WDL/jnetlib/util.o
OBJS += ../../WDL/jnetlib/httpget.o
OBJS += ../../WDL/lameencdec.o
OBJS += ../../WDL/rng.o
OBJS += ../../WDL/sha.o
OBJS += ../mpb.o
OBJS += ../netmsg.o
OBJS += ../njclient.o

OBJS += ../njmisc.o
OBJS += njcast.o
OBJS += ninjamcast.o

CXXFLAGS = $(CFLAGS)

default: ninjamcast

ninjamcast: $(OBJS)
	$(CXX) $(CXXFLAGS) -o ninjamcast $(OBJS) -lpthread $(LFLAGS) -logg -lvorbis -lvorbisenc -lmp3lame

clean:
	-rm $(OBJS) ninjamcast
