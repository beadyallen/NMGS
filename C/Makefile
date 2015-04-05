CC     = gcc
#CFLAGS = -fopenmp -g
CFLAGS = -fopenmp -O3
EFLAGS =  
EFILE  = NMGS
LIBS   = -lm -lgsl -lgslcblas -lgomp
OBJS   = NMGS.o 

$(EFILE) : $(OBJS)
	@echo "linking..."
	$(CC) $(EFLAGS) -o $(EFILE) $(OBJS) $(LIBS)

$(OBJS) : NMGS.c NMGS.h Makefile 
	$(CC) $(CFLAGS) -c $*.c 

clean:
	rm -rf *.o NMGS
