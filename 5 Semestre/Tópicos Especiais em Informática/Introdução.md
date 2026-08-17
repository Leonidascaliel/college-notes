# **Sistemas Monolíticos**
#### **1 — SISTEMAS MONOLÍTICOS TOTALMENTE ACOPLADOS:**

Por padrão um sistema monolítico já é acoplado, mas existe um diferencial em como você modulariza as coisas. Por exemplo: se você está criando um sistema que teve um crescimento orgânico e novas funcionalidades aparecem conforme você trabalha nele, a melhor forma de descobrir se o seu sistema está muito acoplado é pensar se seria difícil eventualmente separá-lo em diversas partes.

Quando os componentes estão muito conectados e os serviços dependem muito uns dos outros, realmente tudo é a mesma coisa. Mas é muito natural que você tenha esse tipo de sistema, principalmente se não houver um planejamento inicial para modularizá-lo.

No fim, a maior característica desse tipo de sistema é que os contextos delimitados (pensando em DDD: Domain-Driven Design) estão todos juntos. Ou seja, você não consegue definir direito quais são as partes do sistema porque tudo está conectado.

Uma vez que esses contextos estejam juntos, a sua empresa e o seu projeto são apenas um. E como tudo é um grande e único contexto, é muito difícil resolver problemas específicos e escalar. Por isso nós temos vontade de excluir esse tipo de sistema e recriar tudo de novo.

E se você está pensando em criar o seu sistema monolítico do zero, provavelmente você tem dois motivos: um é a falta de testes, resultando em bugs quando você altera uma parte e afeta a outra; o outro é que tudo está acoplado dessa forma e alterar uma parte pode causar problemas em outra.

Quando isso acontece é porque você tem um forte indício de que existe essa pequena falha afetando o seu sistema. Ou seja, qualquer coisa que você faz causa um grande efeito colateral para o resto do sistema.

Por isso, nesse tipo de sistema monolítico o mínimo que você deve ter são testes automatizados. E se você não tem isso hoje em dia, apesar de ser um descuido comum, é altamente recomendável que você comece a testar para diminuir esses problemas.

#### **2 — SISTEMAS MONOLÍTICOS SEPARADOS OU MONÓLITOS DISTRIBUÍDOS:**

É o típico sistema monolítico que você quer fazer porque ouviu falar em microsserviços. Nesse caso você acaba criando diversos tipos de sistemas monolíticos, mas que no fim estão todos separados.

A consequência disso é que as dependências ficam tão grandes que para o deploy de apenas um, você precisa fazer o deploy de outro. E você percebe que isso foi um erro grave porque esses elementos devem estar em um único lugar.

Se você pretende trabalhar com esses microsserviços ou algo do tipo, onde os serviços devem subir em conjunto, provavelmente você está na pior das situações por trabalhar de forma separada e com um grande acoplamento.

Nesse tipo de situação o ideal é que você trabalhe com um único sistema monolítico. Isso, na verdade, é chamado de Monólito Distribuído, sendo que ele nem é tão distribuído assim; ele é totalmente separado.

Muitas pessoas ainda utilizam o mesmo banco de dados para fazer esse tipo de sistema, então tome muito cuidado com isso. Essa é a pior situação que você pode estar quando o assunto é desenvolvimento de sistemas.

#### **3 — SISTEMAS MONOLÍTICOS MODULARES:** 

Essa categoria é muito vantajosa porque você acaba separando cada módulo do sistema monolítico para um contexto. Ou seja, você tem e visualiza diversos subdomínios no seu domínio.

Nesse caso você modela os subdomínios em contextos que se comunicam dentro do mesmo sistema, mas fundamentalmente através de contatos e interfaces para que o acoplamento dos subdomínios não seja tão grande.

Nós fazemos isso porque se um dia os contextos evoluírem vai ser muito mais fácil quebrar o domínio em microsserviços, além de gerar menos efeitos colaterais porque cada contexto não precisa necessariamente saber detalhes da implementação de um outro contexto.

Você pode até criar fachadas para estabelecer a comunicação entre os contextos, embora essa alteração faça com que outros contextos não saibam o que está acontecendo. Por isso é vantajoso pensar nos seus sistemas monolíticos como se fossem microsserviços dentro do mesmo sistema.

Lembrando que um sistema monolítico é um sistema que tem a sua unidade de deploy, ou seja, ao fazer o deploy de uma unidade é necessário subir tudo de uma vez, já que essa é uma característica desse tipo de aplicação.

Além de tudo isso você também vai ter a vantagem de escalar times em grande escala onde toda a equipe trabalha em módulos diferentes do mesmo sistema, como se cada membro estivesse trabalhando no seu próprio microsserviço.

Obviamente há mais de uma complexidade em como nós trabalhamos com bancos de dados e mudar uma tabela pode afetar o outro lado do sistema, mas mesmo assim isso não deixa de ser um sistema monolítico e a modularização faz toda a diferença.

Então a modularização não é sobre separar áreas, mas em como separamos os contextos e as suas responsabilidades, como: suporte ao cliente, catálogo de pagamentos e nota fiscal. E isso não tem a ver com tabelas de bancos ou entidades; mas sim de modularizar.

#### **4 — SISTEMAS MONOLÍTICOS MODULARIZADOS, COM MÚLTIPLOS BANCOS DE DADOS OU ESQUEMAS:**

Mesmo que tudo esteja no mesmo sistema, cada contexto possui o seu próprio banco de dados e também fica mais independente de outros contextos.

Nesse caso, se você muda uma coluna no seu banco de dados isso não afeta a coluna do outro contexto no banco de dados. Por outro lado, isso sempre gera efeitos colaterais como a duplicação de dados entre os contextos. Mas quem trabalha com microsserviços sabe que isso é muito natural.

É muito interessante trabalhar com a possibilidade de desfazer uma implementação num sistema fundamentalmente acoplado sem afetar alguma outra coisa, mesmo que em algum momento alguma coisa seja afetada, mas mesmo assim o acoplamento diminui.

A grande vantagem de trabalhar em sistemas monolíticos é tentar diminuir o acoplamento e aumentar a coesão para que as coisas mudem em conjunto e permaneçam assim, mas da forma mais isolada possível.

Quando garantimos isso é possível manter a coesão e desacoplar as coisas que mudam de forma separada, então ao menos nós temos a parte de separar os ‘esquemas’ para deixar as coisas mais independentes umas das outras.

Tudo isso tem um grau de complexidade e nem sempre trabalhar com múltiplos esquemas no mesmo sistema monolítico é a melhor situação, mas modularizar sempre vai ser a melhor opção para você não trabalhar com sistemas monolíticos o tempo todo.

Hoje em dia é difícil não modularizar e a vantagem é que o seu framework vai conseguir atender a todos os módulos simultaneamente, então basicamente: servidor web; sistemas de mensageria; sistemas de validação e etc. Você compartilha tudo isso entre os módulos. Então você deve deixar algo como um shared kernel separado para que todos se beneficiem do framework. Mas não adianta você querer modularizar e modularizar também a parte de bibliotecas compartilhadas, que você pode usar bastante, desde que você se lembre de modularizar os seus negócios.

# AJAX - Asynchronous JavaScript and XML
Um conjunto de técnicas de desenvolvimento web que usa **JavaScript** e **XMLHttpRequest** para trocar dados com um servidor em segundo plano. Isso permite atualizar partes de uma página web sem precisar recarregá-la inteira.

# DOM - Document Object Model
* É como o navegador representa o HTML.
* O HTML vira uma árvore de objetos
### Ideia principal
* Cada tag = um nó do DOM
* JavaScript manipula o DOM, não o HTML direto.
### Qual a finalidade
* Alterar textos e estilos.
* Criar, remover e modificar elementos.
* Responder a eventos (cliques, teclado, etc.)
**AJAX Busca os dados no servidor e atualiza o DOM sem reload.**

# Web Scraping
extração automatizada de dados de sites da web usando Python ou extensões de navegador, transformando código HTML em informações estruturadas. Suas principais aplicações incluem monitoramento de preços, pesquisa de mercado, análise de sentimentos e coleta de notícias.
