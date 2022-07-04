CC:=gcc
CFLAGS:=-Wall
OBJS:=main.o math_functions.o
BIN:=calculator

all:
	$(CC) $(CFLAGS) -c main.c
	$(CC) $(CFLAGS) -c math_functions.c
	$(CC) $(CFLAGS) main.o math_functions.o -o $(BIN)  

clean:
	rm -f $(BIN) $(OBJS)
