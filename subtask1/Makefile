


hello ariel: hello_ariel.o main1_1.o
	gcc hello_ariel.o main1_1.o -o hello_ariel
	
hello_ariel.o: hello_ariel.c hello_ariel.h
	gcc -c hello_ariel.c

main1_1.o: main1_1.c hello_ariel.h
	gcc -c main1_1.c
	
clean:
	rm -f *.o hello_ariel