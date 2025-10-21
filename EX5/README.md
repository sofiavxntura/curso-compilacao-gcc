## Instruções (Makefile)
1. Crie a seção `libProgPag076.a` que, ao ser evocada, gere uma versão estática da biblioteca `libProgPag076`.
2. Crie a seção `progPag076Stat` que, ao ser evocada, gere uma versão do executável original chamada `progPag076Stat`. A linkagem estática deve ser feita entre `libProgPag076.a` e `progPag076.o`.
3. Modifique a seção `clean` para que sejam removidos também os arquivos .a
4. Use `$ ls -la`
5. Rode com `$ make -f Makefile`
