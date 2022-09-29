obj := test1.o test2.o test3.o main.o

ifeq ($(USE_INC), yes)

all-inc: $(obj)
	gcc $^ -o task

include make1.mk
include make2.mk
include make3.mk

else

all-ninc:
	$(MAKE) -f make1.mk
	$(MAKE) -f make2.mk
	$(MAKE) -f make3.mk
	$(MAKE) main.o
	gcc *.o -o task

endif



main.o:
	gcc -c main.c

clean:
	rm -f *.o task
