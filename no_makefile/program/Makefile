CFLAGS:=-Wall
OBJS:=main.o maths.o usage.o
BIN:=calculator

all:calculator

$(BIN):$(OBJS)
	$(CC) $(CFLAGS) -o $@ $^

%.o:%.c
	$(CC) -c $(CFLAGS) $^

clean:
	rm -f $(BIN) $(OBJS)