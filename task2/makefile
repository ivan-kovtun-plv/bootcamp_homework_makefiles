obj := test1.o test2.o test3.o main.o

all: $(obj)
	gcc $^ -o task

main.o:
	gcc -c main.c

include make1.mk
include make2.mk
include make3.mk

all-f:
	$(MAKE) -f make1.mk
	$(MAKE) -f make2.mk
	$(MAKE) -f make3.mk
	$(MAKE) main.o
	gcc *.o -o task

clean:
	rm -f *.o task
