CFLAGS:=-Wall -Werror
BIN:=main
OBJS:=main.o file_reader.o
SOBJS:=libfile_reader.so

all:$(BIN)

$(BIN):main.o
	$(CC) -L. $(CFLAGS) $^ -o $@ -lfile_reader
	export LD_LIBRARY_PATH=./:$LD_LIBRARY_PATH 

main.o:libfile_reader.so
	$(CC) $(CFLAGS) -c main.c 

libfile_reader.so:file_reader.o
	$(CC) -shared -o $@ $^ 

file_reader.o:file_reader.c
	$(CC) -c $(CFLAGS) -fPIC file_reader.c 

clean: 
	$(RM) $(BIN) $(OBJS) $(SOBJS)