### Como é armazenado os dados em diferentes tipos de variáveis?
Variáveis do tipo **Double** é armazenado 8 bytes e no tipo **Float** são 4 bytes. Variáveis do tipo **Char** é possível armazenar apenas 1 byte, armazenando caracteres.

### O que é uma String?
A String já é um tipo de classe, ela funciona diferente de outras variáveis

### Regras
Para mostrar (Print) temos diferentes tipos para representar o dado:
* %d (Double);
* %f (Float);
* %c (Char).

#### Tipos de incompatibilidade de dados
No exemplo "("Idade: " + idade)" temos uma representação de dois tipos de variáveis diferentes, a "Idade" está em **String** e a **"Idade"** concatenada esta em **Int**, entretanto, só é possível atribuir (concatenar ou "somar", representado por "+") através da conversão implícita de dados (CSTR), transformando a **"Idade"** também em **String**, portanto, depois da conversão, é possível concatenar.

	X = (int) (Math.random() * 100);
"**(int)**" = Cast: Modificador de acesso de endereçamento de memória.
**"random"** = Método de classe ou método estático. Gera números entre 0 e 1 (exemplo 0,49985...).
**"Math"** = Classe

#### Bibliotecas Utilizadas
Exemplos em Linguagem C que é utilizado para conceitos em Java também:
	Em C = #include <math.h>
	Em Java = (**Math**.random).
Podem ser chamados de método de classe ou apenas método.

Esse método foi utilizado para gerar randomicamente números aleatórios do tipo **"Double"**, entretanto, precisamos do número em tipo **"Int"**, por isso utilizamos o **"Cast"**, transformando o número de **Double** para **Int** e armazenando na variável **X**.