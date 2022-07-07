CFLAGS:=-Wall -fPIC
LIB:=libcalculator.so
PREFIX:=/usr

all: $(LIB)

$(LIB):calculator.o
	$(CC) -shared -o $@ $^

calculator.o: math_functions.c
	$(CC) -c $(CFLAGS) $^ -o $@ 

install: 
	install -m 755 $(LIB) $(PREFIX)/lib/libcalculator.so
	ldconfig 
	install -m 644 math_functions.h $(PREFIX)/include/math_functions.h

uninstall:
	$(RM) $(PREFIX)/lib/$(LIB)
	$(RM) $(PREFIX)/include/math_functions.h

clean:
	$(RM) $(LIB)
	$(RM) calculator.o
