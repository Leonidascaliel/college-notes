### Bancos Colunares
Os bancos colunares organizam os dados por colunas em vez de linhas. Isso significa que os valores de uma mesma coluna são armazenadas fisicamente juntos, o que permite uma leitura muito mais eficiente quando se deseja acessar apenas algumas colunas específicas de grandes conjuntos de dados.

Esse modelo é especialmente indicado para sistemas analíticos, business intelligence.

* Principais usos
1. Processamento de grandes volumes de dados históricos.
2. aplicações de análise preditiva, mineração de dados e dashboards.
3. armazenamento de logs e métricas de sistemas em tempo real.

* Vantagens
1. Alta performance em consultas analíticas que evoluem grandes volumes de dados
2. boa compressão de dados
3. suporte a escalabilidade horizontal

* Desvantagens
1. Não são indicados para operações transacionais pequenas e frequentes
2. modelo mais complexo para iniciantes

* Exemplo de bancos colunares
1. Apache Cassandra
2. Hbase
3. Google Bigtable


| Aspecto        | Colunar (Cassandra)                             | Relacional (SQL)            |
| -------------- | ----------------------------------------------- | --------------------------- |
| Linguagem      | CQL (Parecida com SQL)                          | SQL                         |
| Esquema Fixo   | Sim, mas mais flexível                          | Sim (Tabelas pré-definidas) |
| Normalização   | Desnormalização (repete dados para performance) | Comum (Evita repetição)     |
| Relacionamento | Não suporta JOINS                               | Com JOINS                   |

### Orientado a Grafos
Os bancos orientados a grafos são uma categoria especial de banco de dados projetada para armazenar e consultar dados altamente conectados.

Em vez de tabelas, documentos ou colunas, os dados são modelados como um grafo, composto por nós (vértices) e arestas(relacionamentos).

### Estrutura Básica
Nó(node) = Representa uma entidade
* Ex: um usuário, um produto, uma cidade.
Aresta (edge) = Representa a relação entre dois nós
* Ex: "é amigo de", "mora em", "comprou".
