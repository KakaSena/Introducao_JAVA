# Entrada de dados do teclado

Como o usuário entra com valores no nosso programa? nessa secção vamos ver como pegar valores vindos do teclado. Teremos 2 tipos de entradas: usando o pacote IO e usando java puro.

## Usando pacote IO
O pacote IO foi feito para simplificar a vida do estudante, nessa parte de pedir valores do teclado ele simplifica bastante. Lembre que antes de todos os programas que usam o pacote IO deve ter a linha **import IO.*;**

### int
Para ler um valor *int* do teclado usamos a [função*](https://github.com/AlexandreVelloso/Introducao_JAVA/edit/master/Entrada%20de%20dados/README.md) *readint*
```
// Somente ler o valor
int num1 = IO.readint();

// Mostrar na tela uma mensagem e ler o valor
int num2 = IO.readint( "Digite um valor inteiro" );

/*
OBS:
No 1 caso o programa vai ficar parado esperando o usuário digitar o valor, se o usuário não saber o que é
para fazer ele pode achar que o programa bugou.
No 2 caso o programa mostra uma mensagem na tela, e ai o usuário vai saber que é para digitar um
valor inteiro do teclado.
Se o usuário digitar algo que não seja um int, como uma letra, string, ou double o valor armazenado será 0.
Esse padrão foi feito pelo professor Theldo.
*/
```

### double

No valor *double* também vale a condição, se o usuário digitar um valor inválido o pacote IO vai colocar 0.0 na variável. Você pode colocar valores inteiros do teclado, e não se esqueça: valores *double* em java são com **.** e não com **,** <br />
Valores válidos: 1, 0.0, 3.14, ...

```
// Somente le o numero do teclado
double num1 = IO.readdouble();
// informa a mensagem e o usuario coloca o numero na mesma linha
double num2 = IO.readdouble( "Digite um valor real: " );
// informa a mensagem e o usuario coloca o numero na linha de baixo
double num3 = IO.readdouble( "Digite outro valor real\n");
```

### char
No *char* é mais difícil de conseguir valores inválidos, pois temos 255 caracteres a nossa escolha na [tabela ascii](http://ic.unicamp.br/%7Eeverton/aulas/hardware/tabelaASCII.pdf), mas se mesmo assim você for animado(a) existem milhares caracteres na codificação [UTF-8](http://www.utf8-chartable.de/unicode-utf8-table.pl?number=1024&utf8=dec) como **Σ** que não existe em ascii, nesse caso o valor armazenado no *char* será um valor inválido e será mostrado como **?**, mas cuidado, isso não quer dizer que é o caractere **?** e sim um caractere inválido.<br />
Se você digitar qualquer coisa maior que um caractere, como o seu nome o pacote IO irá pegar somente o 1º caractere.

```
// Somente le o numero do teclado
char num1 = IO.readchar();
// informa a mensagem e o usuario coloca o numero na mesma linha
char num2 = IO.readchar( "Digite um valor real: " );
// informa a mensagem e o usuario coloca o numero na linha de baixo
char num3 = IO.readchar( "Digite outro valor real\n");
```

### String
```

```

### boolean
```

```

## Usando JAVA puro