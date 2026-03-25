### Estrutura de Herança em Classes
Existe uma estrutura de classes nas heranças de classes dentro da [[Objetos em POO]].

Exemplo:
	Classe A = Super Classe
	Classe B e C = Sub Classe
	Setas da sub classe B e C direcionadas a Super Classe são chamadas de "**Simbologia** **de** **Herança**"

### Implementação de Herança
Para ter um exemplo mais concreto, temos um "Aluno" e um "Professor", o aluno tem as características: 
* Registro Escolar, Nome, Data de Nascimento, Mensalidade. 
E suas operações são:
* Apontar registro escolar, Apontar nome, apontar data de nascimento, Apontar Mensalidade.

Já o professor, suas características são:
* Registro funcional, Nome, Data de Nascimento, Salário.
E suas operações são:
* Apontar registro funcional, Apontar nome, Apontar data de Nascimento, Apontar Salário.

Porém, quando analisamos as duas classes, ambras tem características comuns e específicas, as comuns são "Nome" e "Data de nascimento" e as específicas são as sobressalentes. 
Diante desta situação, na análise do projeto, aplicamos uma técnica chamada de generalização.

### Generalização ou Super Classe
Consiste em concentrar atributos e métodos comuns entre as sub classes (Aluno e professor), através de vínculos de herança. Implementar uma Super Classe é uma boa prática para permitir adaptabilidade e menos custo no seu projeto.

**Dica** **importante**!
	Não se deve inserir/criar novamente os atributos e métodos nas **Sub** **Classes** de uma **Super** **Classe**. Somente os atributos e métodos específicos.

Dentro da **Super** **Classe**, geralmente a definição de acesso aos atributos é **Privada**, mas em alguns momentos, pode ser alterado de "**Privado**" para "**Protegido**", o "**Protegido**" é reconhecido pelo sinal de "**#**" e o "Privado" por "-".

### Criação
Para criar uma "Super Classe" é necessário ter um método construtor. Em java é utilizado o comando "Super" para referenciar a Super Classe. Em C# é utilizado o comando "Base".