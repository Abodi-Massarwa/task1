all: Static Dynamic

Static: libhello.a main1_1.o
	gcc main1_1.o -o Static libhello.a

Dynamic: libhello.so main1_1.o
	gcc  main1_1.o -o Dynamic ./libhello.so

libhello.so:hello_ariel.o
	gcc -shared hello_ariel.o -o libhello.so
	

libhello.a: hello_ariel.o
	ar rcs libhello.a hello_ariel.o
	
hello_ariel.o: hello_ariel.c hello_ariel.h
	gcc -g -Wall -c hello_ariel.c -fpic

main1_1.o: main1_1.c hello_ariel.h
	gcc -g -Wall -c main1_1.c -fpic
	
clean:
	rm -f *.o  *.a *.so Dynamic Static
	