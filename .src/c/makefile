CC=cc
FLAGS= -std=c99 -W -O2 -g -Wextra 
EFLAGS= -s -save-temnps -O2 -Werror

default:
	$(CC) $(args) -o main $(FLAGS)

bin: binHeaders.o
	$(CC) -c $(args) -o main.o
	$(CC) main.o binHeaders.o -o main $(FLAGS)
binHeaders.o:
	$(CC) -c binHeaders.c binHeaders.h 

debug:
	$(CC) $(args) -o main $(EFLAGS) $(FLAGS)

debugbin : binHeaders.o
	$(CC) $(args) -o main $(EFLAGS) $(FLAGS)

Clean:
	@rm main
	@rm *.o
	@rm *.gch
