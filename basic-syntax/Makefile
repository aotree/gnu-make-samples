CFLAGS = -O0

foo: foo.o main.o
	cc -o foo foo.o main.o

foo.o: foo.c foo.h
	cc -c $(CFLAGS) -o foo.o foo.c

main.o: main.c foo.h
	cc -c $(CFLAGS) -o $@ $<

.PHONY: clean # Enamurate task targets that don't represent file names.
clean:
	rm -f foo *.o
