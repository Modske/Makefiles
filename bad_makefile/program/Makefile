CFLAGS:=-Wall -Werror
OBJS:=main.o math_functions.o
BIN:=calculator

all:$(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

%.o:%.c
	$(CC) -c $(CFLAGS) $^

clean:
	$(RM) $(BIN) $(OBJS)

