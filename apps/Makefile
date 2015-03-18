CC = gcc

CFLAGS = -std=gnu99 -Wall -Wno-unused-parameter -Wno-unused-function -pthread -I/usr/local/include/libcapriltag/ -I/usr/local/include/libcapriltag/common -O1
LDFLAGS = -lpthread -lm -L/usr/local/lib/ -lcapriltag -Wl,--no-as-needed

all: apriltag_demo

apriltag_demo:
	$(CC) -o apriltag_demo apriltag_demo.c $(CFLAGS) $(LDFLAGS)