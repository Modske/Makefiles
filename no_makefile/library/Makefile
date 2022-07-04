CC:=gcc
CFLAGS:=-Wall
BIN:=main
OBJS:=main.o file_reader.o
SOBJS:=libfile_reader.so

all:main

main:main.o
	$(CC) -L. $(CFLAGS) main.o -o main -lfile_reader

main.o:libfile_reader.so
	$(CC) $(CFLAGS) -c main.c

libfile_reader.so:file_reader.o
	$(CC) -shared -o libfile_reader.so file_reader.o 
	export LD_LIBRARY_PATH='pwd':$LD_LIBRARY_PATH 

file_reader.o:file_reader.c
	$(CC) -c $(CFLAGS) file_reader.c 

clean: 
	rm -f $(BIN) $(OBJS) $(SOBJS)

lib:libfile_reader.so