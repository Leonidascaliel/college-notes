### A implantação no mundo real (Cliente)
A Visão física, também conhecida como visão de implantação (Deployment), descreve como o software mapeado no hardware e na infraestrutura de rede. Ela detalha a topologia do sistema, mostrando os nós físicos e as conexões de comunicação entre eles.

#### Elementos fundamentais
* Nós (Nodes), Servidores, VMs, Contêineres, Dispositivos.
* Artefatos de implantação: Executáveis, bibliotecas, scripts.
* Links de comunicação: Conexão de rede, protocolos.

#### Stakeholders
* Engenheiros de sistemas.
* Administradores de rede.
* Equipes de DevOps.

#### Notações
* Diagramas de implantação (UML).
* Diagramas de arquitetura de nuvem.
* Infraestrutura como Código (IaC).

### Exemplo Prático
### Implantação em Nuvem com Alta Disponibilidade
Para nosso sistema de e-commerce, uma visão física robusta e implantado na AWS poderia ser:
* Regions: sa-east-1
* Availability Zones
* Load Balancer (ELB)
* Auto Scalling Group (EC2)
* Banco de Dados (RDS)
* Fila de mensagens (SQS)

### Sugestões para aprofundamento
* Padrões arquiteturais
* Atributos de qualidade
* Normas e frameworks