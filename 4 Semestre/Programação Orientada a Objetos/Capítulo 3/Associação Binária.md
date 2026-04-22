### O que é uma Associação Binária?
A Associação Binária estabelece uma ligação (Apontamento - "Ponteiro") entre objetos de duas classes distintas. E a associação binária pode ser do tipo:
* Associação Binária Unidirecional
* Associação Binária Bidirecional

#### Associação Unidirecional
Indica que o objeto de uma classe aponta para um ou mais objetos de uma outra classe.

Exemplo: um (1) objeto da classe A aponta (->) para um (1) objeto da classe B.

#### Associação Bidirecional
Indica que um objeto de uma classe aponta para um ou mais objetos de uma outra classe. Contudo, o objeto apontado, aponta para um ou mais objetos da classe cujo o objeto está realizando o apontamento.

*Exemplo: (1) objeto da classe C aponta (->) para um ou mais (1...*) objetos da classe D.
Contudo, um (1) da classe D aponta (->) para um (1) objeto da classe C.*

Se o (1...) conter "Asterisco", significa que são múltiplos ponteiros.

#### Multiplicidade
Indica quantas instancias (objetos) estão ligadas a outra classe.

*Exemplo: 0...1, 1, 0...(Asterisco)*, (Asterisco), 1...(Asterisco), 1..., 15(m...n). 