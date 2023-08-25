# AWS - Resumo Treinamento AWS

Anotações referentes ao curso AWS Cloud Practitioner na plataforma AWS Skill Builder.

## Bancos de Dados AWS

A AWS fornece suporte para conexão com os mais variados sistemas **RDBS** ou sistemas de banco de dados relacionais por meio de um EC2 por meio da técnica de `lift-and-shift` ou então executar banco de dados com um maior gerenciamento pelo **`AWS RDS`** ou Amazon Relational Database Service. Ambos são compatíveis com os principais mecanismos de banco de dados como MySQL, PostgreSQL, Oracle, Microsoft MSQL, entre outros.

### AWS RDS - Relational Database Service

Serviço que permite executar banco de dados relacionais na nuvem AWS, sendo um serviço altamente gerenciado que automatiza tarefas como provisionamento de hardware, configurações, patchs, backups, redundância failover, etc. Podendo-se integrar a outros serviços AWS como AWS Lambda para consultar o banco de dados, fornecendo inúmeras opções diferentes de segurança como criptografia em repouso e em trânsito. Compatível com os mecanismos Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle e Microsoft SQL Server.

> Amazon Aurora

Banco de dados relacional de nível empresarial compatível com MySQL (Aurora é 5x mais rápido) e PostgreSQL (Aurora é 3x mais rápido). Ajuda a reduzir custos por redução de operações desnecessárias de entrada/saída sendo confíavel e disponível. Ideal para cargas de alta disponibilidade replicando 6 cópias dos dados em 3 AZ's além de fazer backup contínuo dos dados para o S3.

### AWS DynamoDB

Serviço de banco de dados **NOSQL** por chave-valor, oferecendo um desempenho de 1 dígito de milissegundo em qualquer scaling. Não tem a neccesidade de gerenciamento por ser serverless nem instalar, manter ou operar o software. Escala automaticamente dimensionando para ajustar as alterações da capacidade porém mantendo o desempenho consistente.

### AWS Redshift

Serviço de Data warehouse com escalabilidade massiva para análise de big data tendo os sues nós alcançando vários petabytes em escala. Com o auxílio do **AWS Redshift Spectrum** pode-se rodar uma única consulta SQL em Hexabytes de dados não estruturados diretamente no Data link. Tem uma performance 10x maior do que banco de dados tradicionais.

### AWS DMS - Database Migragtion Service

Fornece migração de um banco de dados on-premises ou já na AWS para a nuvem AWS, de forma segura e fácil. O banco de origem permanece intacto e operacional durante a migração. Pode-se utilizar para criar um banco de teste, combinar vários bancos em um só e replicação contínua com cópias dos dados para outra fonte de destino ao invés de migração única.

- Migração homogênea

      São migrações entre o banco de destino e de origem que são do mesmo tipo, exemplo do Oracle para o RDS Oracle, são 
      simples pelo fato da estrutura do schema, tipos de dados e código do banco serem compatíveis entre os bancos.

- Migração heterogênea

      Processo em duas eatpas em que a primeira consiste em converter o schema e o código do banco utilizando a ferramenta
      AWS Schema Convertion Tools, em segundo migramos os dados entre os bancos utilizando o serviço AWS DMS

### Outros Bancos AWS

- **AWS DocumentDB**: serviço de banco de dados de documentos compatível com cargas de trabalho do **MongoDB**.
- **AWS Neptune**: cria e executa aplicativos que funcionam com conjuntos de dados altamente conectados. Banco de dados em grafo.
- **AWS QLDB (Quantum Ledger)**: revisa históricos completos de todas alterações nas aplicações, com oss registros sendo imutáveis.
- **AWS Managed Blockchain**: cria e gerencia redes de blockchain com estruturas de código aberto.
- **AWS ElasticCache**: adiciona camadas de cache e melhora o tempo de leitura de solicitações comuns. Compatível com Redis e Memcached.
- **AWS DynamoDB Accelerator (DAX)**: cache em memória para o DynamoDB, ajudando a melhorar os tempos de resposta de ms para microssegundos

## Segurança



