Este é um simples Analisador Léxico criado para a disciplina de Paradigmas de Linguagem de programação.

Este Analisador Léxico lê um programa fonte a partir de um arquivo com extensão ".cpt" (C português).
O arquivo de saída é gravado em um arquivo texto comm extensão ".ctk" (C tokens).

O Analisador Léxico reconhece os tokens apresentados na tabela abaixo

IDENTIFICADOR | TOKEN | LEXEMA
--------------|-------|--------
1| IDENTIFICADOR|
2| INTEIRO|
3| REAL|
4| CARACTER|
5| CADEIA_CARACTERES|
6| ATRIBUICAO| <-
7| SOMA| +
8| SUBRITACAO| -
9| MULTIPLICACAO| *
10| DIVISAO| /
11| POTENCIA| ^
12| SE| se
13| ENQUANTO| enquanto
14| PARA| para
15| INICIO_ESCOPO| {
16| FIM_ESCOPO| }
17| INICIO_PARAMETRO| (
18| FIM_PARAMETRO| )
19| TIPO| int, real, caracter, vazio
20| COMENTARIO_LINHA| //
21| INICIO_COMENTARIO_PARAGRAFO| /*
22| FIM_COMENTARIO_PARAGRAFO| */
23| FIM_COMANDO| ;
24| VIRGULA| ,
25| ENTRADA_PADRAO| Teclado
26| SAIDA_PADRAO| Tela
27| COMPARACAO| =
28| SENAO| senao
29| RETORNO_FUNCAO| retornar
30| PRINCIPAL| principal
31| RESTO_DIVISAO| %
32| MENOR| <
33| MENOR_IGUAL| <=
34| MAIOR| >
35| MAIOR_IGUAL| >=


Exemplos de programas a serem reconhecidos:

```sh
vazio principal () {
  int a, b;
  tela <- “Informe o primeiro número:”;
  a <- teclado;
  tela <- “Informe o segundo número:”;
  b <- teclado;
  se (a > b)
    tela <- “Maior: ” + a;
  senao
    tela <- “Maior: ” + b;
}
```