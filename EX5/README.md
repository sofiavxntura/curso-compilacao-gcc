## Instruções (Makefile)
1. Crie a seção `libProgPag076.a` que, ao ser evocada, gere uma versão estática da biblioteca `libProgPag076`.
2. Crie a seção `progPag076Stat` que, ao ser evocada, gere uma versão do executável original chamada `progPag076Stat`. A linkagem estática deve ser feita entre `libProgPag076.a` e `progPag076.o`.
3. Modifique a seção `clean` para que sejam removidos também os arquivos .a
4. Use `$ ls -la`.
5. Rode com `$ make -f Makefile` e `$ make clean` caso queira limpar os aquivos correspondentes com os parâmetros colocados no código..

## Resolução
- No clean, usei `*a` em `rm *.o *.a *.so`
- Criei `mychio.o` para garantir que erros nao acontecessem
   ```
      mychio.o: mygetop.c mypushpop.c mychio.c
                gcc mygetop.c mypushpop.c mychio.c
    ```
- Criei `libProgPag076.a`
  ```
    libProgPag076.a: mychio.o mypushpop.o mygetop.o
                    ar rcs libProgPag076.a mychio.o mypushpop.o mygetop.o
  ```
  
