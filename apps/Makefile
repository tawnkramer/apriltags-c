CC = gcc

CFLAGS = -c -std=gnu99 -Wall -Wno-unused-parameter -Wno-unused-function -pthread -I../ -I../common -O1
LDFLAGS = -L.. -lcapriltag -lpthread -lm

TARGET = apriltag_demo

.PHONY: default all clean

default: $(TARGET)
all: $(TARGET)

OBJECTS = $(patsubst %.c, %.o, $(wildcard *.c))
HEADERS = $(wildcard *.h)

%.o: %.c $(HEADERS)
	$(CC) $(CFLAGS) -c $< -o $@

.PRECIOUS: $(TARGET) $(OBJECTS)

$(TARGET): $(OBJECTS)
	$(CC) $(OBJECTS) $(LDFLAGS) -o $@

clean:
	-rm -f *.o
	-rm -f $(TARGET)
