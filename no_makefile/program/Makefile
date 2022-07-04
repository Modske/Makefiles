CC:=gcc
CFLAGS:=-Wall
OBJS:=main.o maths.o usage.o
BIN:=calculator

all:
	$(CC) $(CFLAGS) -c main.c
	$(CC) $(CFLAGS) -c usage.c
	$(CC) $(CFLAGS) -c maths.c
	$(CC) $(CFLAGS) main.o usage.o maths.o -o $(BIN)

clean:
	rm -f $(BIN) $(OBJS)