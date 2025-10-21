LIBS=./libProgPag076.so
PROG=progPag076

progPag076Stat: progPag076.c libProgPag076.a 		
	gcc progPag076.c libProgPag076.a -o progPag076Stat --static

progPag076: progPag076.o libProgPag076.so
		gcc progPag076.o ${LIBS} -o ${PROG}

progPag076.o: progPag076.c
		gcc progPag076.c -c

libProgPag076.so: mychio.h mychio.c mypushpop.c mypushpop.h mygetop.c mygetop.h
		gcc mychio.c mypushpop.c  mygetop.c -shared -fPIC -o libProgPag076.so

libProgPag076.a: mychio.o mypushpop.o mygetop.o 
		ar rcs libProgPag076.a mychio.o mypushpop.o mygetop.o

mychio.o: mygetop.c mypushpop.c mychio.c
	gcc mygetop.c mypushpop.c mychio.c -c

clean:
		rm *.o *.a *.so ${PROG}
