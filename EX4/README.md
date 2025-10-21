## Instruções

#### 1.
```
$ gcc mygetop.c mypushpop.c mychio.c -c
$ ls -la
```

#### 2.
```
$ ar rcs libProgPag076.a mygetop.o mypushpop.o mychio.o
$ ls -la
```

#### 3.
```
$ gcc mychio.c mypushpop.c mygetop.c -shared -fPIC -o libProgPag076.so
$ ls -la
```
#### 4.
```
$ gcc progPag076.c libProgPag076.a -o progPag076Stat --static
$ ls -la
```

#### 5.
```
$ ./progPag076Stat
// colocar input -> ex.: 10 20 * (calculadora)
```

#### 6.
```
$ gcc progPag076.c ./libProgPag076.so -o progPag076Dina
$ ls -la
```

#### 7.
```
$ ./progPag076Dina
//input -> ex.: 23 52 * 15 -
```

#### 8.
```
$ objdump -a libProgPag076.a
```

#### 9.
```
$ objdump -tT libProgPag076.so
```

#### 10.
```
$ ldd progPag076Dina
```
