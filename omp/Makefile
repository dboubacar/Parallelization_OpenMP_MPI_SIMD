CC= gcc
CFLAGS= -O3 -Wall -Wextra -g
EXEC= cg_omp
OBJ= mmio.o cg.o
LIB= -lm -fopenmp

all: $(OBJ)
	$(CC) $(CFLAGS)  $(OBJ) -o $(EXEC) $(LIB)


cg.o: cg.c
	$(CC) -c $(CFLAGS) $< $(LIB)

mmio.o: ../lib/mmio.c ../lib/mmio.h
	$(CC) -c $(CFLAGS) ../lib/mmio.c  $(LIB)


.PHONY: clean

clean :
	rm -rf $(EXEC) *~ *.o
