obj := main.o src1.o src2.o

all: $(obj)
	gcc $^ -o task

%.o: %.c
	gcc -c $^

clean:
	rm -f *.o task

