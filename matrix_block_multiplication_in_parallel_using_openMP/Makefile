
UNAME = $(shell uname)

ifeq ($(UNAME), Darwin)
    LIB =
else
    # do this on ADA:
    #
    #       module load intel/2017A
    #       make
    #
    CC = icc -fopenmp
    LIB = -lm -ldl -lrt
endif

SRC = mult.c tictoc.c

stuff:
	echo $(UNAME)
	$(CC) -O3 $(CFLAGS) $(SRC) -o mult $(LIB)
	./mult

