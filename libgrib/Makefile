# Makefile

.PHONY: all clean

CC=gcc
CFLAGS=-ggdb -Wall -Wextra -ansi -pedantic -I. -I$(HOME)/tmp/grib_libraries/local/include

all : libgrib.a

libgrib.a : grib1_unpack.o grib2_unpack.o bits.o conv_float.o grib2_conv.o grib1_write.o
	ar rcs $@ $^

clean :
	rm -f *.o
	rm -f libgrib.a

%.o : %.c
	$(CC) -o $@ -c $< $(CFLAGS)

