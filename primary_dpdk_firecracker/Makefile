PKGCONF = pkg-config
SERVER = server
READER = reader

SRCS_SERVER-y := server.c
SRCS_READER-y := reader.c

CFLAGS += -g -O3 -mssse3 $(shell $(PKGCONF) --cflags libdpdk)
LDFLAGS += $(shell $(PKGCONF) --libs libdpdk)

$(SERVER): $(SRCS_SERVER-y) Makefile
	$(CC) $(CFLAGS) $(SRCS_SERVER-y) -o $@ $(LDFLAGS)

$(READER): $(SRCS_READER-y) Makefile
	$(CC) $(CFLAGS) $(SRCS_READER-y) -o $@ $(LDFLAGS)
