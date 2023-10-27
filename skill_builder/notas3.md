# AWS - Anotações gerais

Anotações referentes ao curso [AWS Cloud Practitioner Essentials](https://explore.skillbuilder.aws/learn/course/8287/elementos-essenciais-do-aws-cloud-practitioner-portugues-aws-cloud-practitioner-essentials-portuguese) na plataforma AWS Skill Builder.

## Bancos de Dados AWS

A AWS fornece suporte para conexão com os mais variados sistemas **RDBS** ou sistemas de banco de dados relacionais por meio de instâncias EC2 ou por meio da técnica de `lift-and-shift`, assim também como executando banco de dados com um maior gerenciamento pelo **`AWS RDS`** ou Amazon Relational Database Service. Ambos são compatíveis com os principais mecanismos de banco de dados como MySQL, PostgreSQL, Oracle, Microsoft MSQL, entre outros.

### AWS RDS - Relational Database Service

Serviço que permite executar banco de dados relacionais na nuvem AWS, sendo um serviço altamente gerenciado que automatiza tarefas como provisionamento de hardware, configurações, patchs, backups, redundância failover, etc. Podendo-se integrar a outros serviços AWS como AWS Lambda para consultar o banco de dados, fornecendo inúmeras opções diferentes de segurança como criptografia em repouso e em trânsito. Compatível com os mecanismos Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle e Microsoft SQL Server.

### Amazon Aurora

Banco de dados relacional de nível empresarial compatível com MySQL (Aurora é 5x mais rápido) e PostgreSQL (Aurora é 3x mais rápido). Ajuda a reduzir custos por redução de operações desnecessárias de entrada/saída sendo confíavel e disponível. Ideal para cargas de alta disponibilidade replicando 6 cópias dos dados em 3 AZ's além de fazer backup contínuo dos dados para o S3.

### AWS DynamoDB

Serviço de banco de dados **NOSQL** por chave-valor, oferecendo um desempenho de 1 dígito de milissegundo em qualquer scaling. Não tem a neccesidade de gerenciamento por ser serverless nem instalar, manter ou operar o software. Escala automaticamente dimensionando para ajustar as alterações da capacidade porém mantendo o desempenho consistente.

### AWS Redshift

Serviço de Data warehouse com escalabilidade massiva para análise de big data tendo os seus nós alcançando vários petabytes em escala. Com o auxílio do **AWS Redshift Spectrum** pode-se rodar uma única consulta SQL em Hexabytes de dados não estruturados diretamente no Data link. Tem uma performance 10x maior do que banco de dados tradicionais.

### AWS DMS - Database Migragtion Service

Fornece migração de um banco de dados on-premises ou já na AWS para a nuvem AWS, de forma segura e fácil. O banco de origem permanece intacto e operacional durante a migração. Pode-se utilizar para criar um banco de teste, combinar vários bancos em um só e replicação contínua com cópias dos dados para outra fonte de destino ao invés de migração única.

- Migração homogênea

      São migrações entre o banco de destino e de origem que são do mesmo tipo, exemplo do Oracle para o RDS Oracle, são 
      simples pelo fato da estrutura do schema, tipos de dados e código do banco serem compatíveis entre os bancos.

- Migração heterogênea

      Processo em duas etapas em que a primeira consiste em converter o schema e o código do banco utilizando a ferramenta
      AWS Schema Convertion Tools, em segundo migramos os dados entre os bancos utilizando o serviço AWS DMS.

### Outros Bancos AWS

- **AWS DocumentDB**: serviço de banco de dados de documentos compatível com cargas de trabalho do **MongoDB**.
- **AWS Neptune**: cria e executa aplicativos que funcionam com conjuntos de dados altamente conectados. Banco de dados em grafo.
- **AWS QLDB (Quantum Ledger)**: revisa históricos completos de todas alterações nas aplicações, com oss registros sendo imutáveis.
- **AWS Managed Blockchain**: cria e gerencia redes de blockchain com estruturas de código aberto.
- **AWS ElastiCache**: adiciona camadas de cache e melhora o tempo de leitura de solicitações comuns. Compatível com Redis e Memcached.
- **AWS DynamoDB Accelerator (DAX)**: cache em memória para o DynamoDB, ajudando a melhorar os tempos de resposta de ms para microssegundos.

## Modelo de Responsabilidade Compartilhada

Basicamente divide-se em responsabilidades da AWS (segurança da nuvem) e do cliente (segurança na nuvem). A AWS opera, gerencia e controla todas as camadas da infraestrutura como SO do host, camada de rede, camada de virtualização e segurança física dos data centers. O cliente são responsáveis pela segurança de tudo que colocam na nuvem AWS, mantendo o controle total sobre o conteúdo e sendo responsável por gerenciar os requisitos de segurança como acessos e revogações.

### IAM (Identity and Access Management)

O IAM oferece o gerenciamento dos acessos aos serviços AWS, com flexibilidade e utilizando uma combinação de recursos como:

- usuários, grupos e roles
- políticas
- autenticação multifator

> Usuário root

    Usuário padrão criado no momento da criação da conta AWS, podendo acessar qualquer recurso na conta. Sendo recomendado não
    utilizar esse usuário para funções gerais e cotidianas.

> Usuário do IAM

    Usuários funcionais que vão realizar as tarefas cotidianas como executar instâncias EC2 ou buckets S3, quando criados não 
    possuem permissões associadas. Recomendado seguir o princípio de menor privilégio ao conceder permissões.

> Políticas (Policies)

    Documento JSON que fornece ou nega permissões para serviços AWS, permitindo personalizar os níveis de acesso ao usuários.
    A política sempre terá o campo Effect que receberá o valor allow ou deny e no campo resource ira declarar a qual serviço
    AWS a política se aplicará.

> Grupos

    Agrupamentos de usuários com permissões comuns entre os mesmos, todos os usuários presentes no grupo herdarão as mesmas
    permissões. Sendo mais fácil adicionar os usuários há um grupo do que criar um política para cada usuário.

> Roles

    Permissões associadas que permitem ou negam ações específicas que podem ser assumidas temporariamente. Pode ser atribuída
    a usuários, entidades externas, aplicações e até serviços AWS, que assumindo-se uma role todas as permissões anteriores
    são abondonadas.

> Autenticação multifator (MFA)

    Fornece uma camada adicional de segurança para a conta AWS, tendo o usuário realizar uma entrada autenticada através de
    um dispositivo configurado que pode ser uma chave de segurança de hardware ou dispositivo de hardware como um telefone.

### Organizations

Centraliza o gerenciamento de várias contas AWS facilmente onde a primeira conta é a raíz servindo como um contêiner para as demais contas. Podendo-se agrupar hierárquicamente contas em unidades organizacionais para atender requisitos de conformidade, segurança e necessidades orçamentais, essas unidades são conhecidas como **`OU`**. Também existe a vantagem das **Políticas de Controle de Serviços (SCPs)** que especificam as permissões máximas das contas, restringindo quais serviços AWS, recursos e ações individuais de APIs que podem ser acessadas, são aplicadas a OUs e a uma conta de membro individual.

### Compliance

Conformidade na AWS abrange uma visão de monitoramento continuo do ambiente utilizando verificações de conformidade automatizadas com base nas práticas recomendadas e nos padrões do setor adotado por sua organização. Os serviços AWS registram 600 bilhões de eventos de API de auditoria todos os dias e 5 bilhões de verificações de configurações de recursos por mês. Fornecendo os seguintes benefícios para os usuários:

- coleta e verificação de dados de auditoria com facilidade
- correção de não conformidades rapidamente
- criação de logs auditáveis aumentando a postura de segurança

### AWS Artifact

Serviço que fornece acesso sob demanda a relatórios de segurança e conformidades AWS assim como a contratos on-line selecionados. Possui duas seções principais: AWS Artifact Agreements e o AWS Artifact Reports, o AWS Artifact fornece vários relatórios de conformidade e regulamentações para uso como ISO, CSA, PCI entre vários outros.

- Artifact Agreements 

      Contrato com a AWS em relação ao uso de determinados tipos de informações em todos os serviços, podendo-se revisar, 
      aceitar e gerenciar contratos para uma conta individual e para todas as contas no AWS Organizations.

- Artifact Reports

      Fornece relatórios de conformidade por auditores terceirizados que testaram e verificaram se a AWS está em conformidade
      com diversas normas e regulamentações de segurança globais, regionais e específicas do setor. Permanece atualizado 
      constantemente.

### Centro de conformidade

Central para acessos de whitepapers e documentações de conformidades AWS relacionados a problemas principais, visão geral de riscos, listas de verificações de segurança de auditorias e plano de aprendizagem para auditores para indivíduos em funções jurídicas, de auditoria e de conformidade.

### DoS - Denial of Services

Ataque de negação de serviços é uma tentativa deliberada de tornar um site ou aplicativo indisponível para os seus usuários, inundando um site ou aplicativo com tráfego excessivo de rede até que o mesmo não consiga mais responder, causando a negação do serviço para o usuário. `São originados de uma única fonte`.

### DDoS - Distributed Denial of Services

Ataque distribuído de negação de serviços onde um ou vários atacantes iniciam o ataque visando tornar um site ou aplicativo indisponível, utilizando vários computadores infectados (bots) para enviar tráfego excessivo ao site ou aplicativo. `São originados de várias fontes` e podem ser combatidos pelo serviço AWS Shield.

### AWS Shield

Serviço que protege aplicativos contra ataques DDoS oferecendo dois tipos de proteções distintas: Standard e Advanced.

> Shield Standard

      Protege automaticamente todos os clientes AWS de ataques DDoS mais frequentes e comuns com custo zero, utiliza diversas
      técnicas de análise para detectar tráfego mal-intencionado em tempo real mitigando-o automaticamente.

> Shield Advanced

      Fornece diagnósticos detalhados e capacidade de detectar e mitigar ataques DDoS elaborados, se integra com diversos
      outros serviços AWS como CloudFront, Route 53 e ELB além do AWS WAF escrevendo regras personailizadas contra ataques.

### Serviços de segurança adicionais

> AWS KMS - Key Management Service

      Permite executar operações de criptografia pelo uso de chaves criptografadas, que é uma cadeia aleatório de dígitos
      utilizada para criptografar (bloquear) e descriptografar (desbloquear) dados. Permite especificar níveis de controle de
      acessos e funções IAM, assim como desativar temporariamente as chaves.

> AWS WAF - Web Application Firewall

      Permite monitorar solicitações e tráfego de rede trabalhando em conjunto com o AWS CloudFront e um balanceador de carga
      utilizando uma lista ACL para proteger os recursos AWS e bloqueando solicitações específicas. Auxilia na proteção contra
      ataques de SQL injection.

> AWS Inspector

      Fornece avaliações automatizadas de segurança e conformidades, verificando vulnerabilidades de segurança e desvios das
      práticas recomendadas. Depois da avaliação fornece uma lista de descobertas que é priorizada pelo nível de gravidade.

> AWS GuardDuty

      Fornece detecção inteligente de ameaças para infraestrutura e recursos AWS, identificando ameaças monitorando 
      continuamente a atividade e comportamento de rede como logs de fluxo de VPC e DNS. Também pode configurar as funções
      para executar etapas de correções automáticas em resposta a descobertas de possíveis ameaças. 
