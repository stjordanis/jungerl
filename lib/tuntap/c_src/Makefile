include ../../../support/include.mk

CFLAGS += -I $(ERL_C_INCLUDE_DIR) -I../../../support

TUN_DRV_SO = ../priv/tun_drv.so
TUNCTL = ../priv/tunctl

all: $(TUN_DRV_SO) $(TUNCTL)

$(TUN_DRV_SO): tun_drv.c
	$(CC) $(CFLAGS) -o $@ -shared -fpic $(ERL_INCLUDE) $<

$(TUNCTL): tunctl.c
	$(CC) $(CFLAGS) -o $@ $<

clean:
	-rm $(TUN_DRV_SO) $(TUNCTL)

.INTERMEDIATE: tun_drv.o

