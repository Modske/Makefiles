CC:=gcc
CFLAGS:=-Wall -fPIC
LIB:=libcalculator.so
PREFIX:=/usr/local

all: $(LIB)

$(LIB):math_functions.o
	$(CC) -shared -o $(LIB) math_functions.o

calculator.o: math_functions.c
	$(CC) -c $(CFLAGS) math_functions.c -o  

install: 
	sudo install -o root -g root -m 755 libcalculator.so $(PREFIX)/lib/libcalculator.so
	sudo ldconfig 
	sudo install -o root -g root -m 644 math_functions.h $(PREFIX)/include/math_functions.h

uninstall:
	sudo rm $(PREFIX)/lib/$(LIB)
	sudo rm $(PREFIX)/include/math_functions.h

clean:
	rm -f $(LIB)
	rm -f math_functions.o
