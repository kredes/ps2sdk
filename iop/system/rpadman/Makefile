# _____     ___ ____     ___ ____
#  ____|   |    ____|   |        | |____|
# |     ___|   |____ ___|    ____| |    \    PS2DEV Open Source Project.
#-----------------------------------------------------------------------
# Copyright 2001-2004, ps2dev - http://www.ps2dev.org
# Licenced under Academic Free License version 2.0
# Review ps2sdk README & LICENSE files for further details.

IOP_OBJS_DIR = obj/
IOP_BIN_DIR = irx/
IOP_SRC_DIR = $(PS2SDKSRC)/iop/system/freepad/src/
IOP_INC_DIR = include/

IOP_BIN = $(IOP_BIN_DIR)rpadman.irx

IOP_CFLAGS += -DSIO2MAN_V2=1 # -DDEBUG

IOP_INCS += -I$(PS2SDKSRC)/iop/system/sio2log/include/ -I$(PS2SDKSRC)/iop/system/rsio2man/include/

IOP_OBJS = freepad.o rpcserver.o exports.o imports.o padInit.o padPortOpen.o padMiscFuncs.o sio2Cmds.o padData.o padCmds.o
IOP_OBJS := $(IOP_OBJS:%=$(IOP_OBJS_DIR)%)

all: $(IOP_OBJS_DIR) $(IOP_BIN_DIR) $(IOP_BIN)

clean:
	rm -f -r $(IOP_OBJS_DIR) $(IOP_BIN_DIR)

include $(PS2SDKSRC)/Defs.make
include $(PS2SDKSRC)/iop/Rules.make
include $(PS2SDKSRC)/iop/Rules.release
