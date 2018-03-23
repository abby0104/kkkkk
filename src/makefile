# makefile example

CC = gcc
CFLAGS = -g -c
AR = ar
INCLUDE = -I../inc
LIBS = -L./ -lmyio
LIBTARGET = libmyio.a

SRC = read.c write.c main.c
OBJ = $(SRC:.c=.o)

.SUFFIXES:.c.o
.c.o:
	$(CC) $(CFLAGS) $(INCLUDE) $<
	
all : test

test : $(OBJ) $(LIBTARGET)
	gcc -o $@ $(OBJ) $(LIBS)

$(LIBTARGET): $(OBJS)
	$(AR) rcv $@ $(OBJS)

clean :
	rm test
	rm *.o
