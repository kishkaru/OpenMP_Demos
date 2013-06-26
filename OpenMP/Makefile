CC=gcc
CFLAGS=-fopenmp -O3 -g -std=c99
LDFLAGS=-fopenmp

all: vadd vadd_OmpNaive vadd_OmpBetter vadd_OmpFor dotp dotp_critical dotp_reduction

vadd: vadd.o

vaddOmpNaive: vaddOmpNaive.o

vaddOmpBetter: vaddOmpBetter.o

vaddOmpFor: vaddOmpFor.o

dotp: dotp.o

dotp2: dotp2.o

clean:
	rm -f vadd vadd_OmpNaive vadd_OmpBetter vadd_OmpFor vadd.o vadd_OmpNaive.o vadd_OmpBetter.o vadd_OmpFor.o dotp dotp.o dotp_critical dotp_reduction dotp_critical.o dotp_reduction.o
	
