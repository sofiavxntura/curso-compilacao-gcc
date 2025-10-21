## Instruções
#### 1.
```
$gcc seno.c -o seno -lm
$ls -la
```

#### 2.
```
$gcc seno.c -o senoDin1 -lm
$ls -la
```

#### 3.
```
$gcc seno.c -o senoDin2 /usr/lib/x86_64-linux-gnu/libm.so
$ls -la
```

#### 4.
```
$gcc seno.c -lm --static -o senoStat
$ls -la
```

#### 5.
```
$gcc seno.c /usr/lib/x86_64-linux-gnu/libm.a --static -o senoStaDin
$ls -la
```
