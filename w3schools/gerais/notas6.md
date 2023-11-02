# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## AWS Cloud Redshift

É um serviço de análise de big data que pode coletar informações de várias fontes e auxilia você a obter conexões entre seus dados. O AWS Redshift é baseado em SQL, com hardware projetado pela AWS e aprendizado de máquina, ótimo quando os dados se tornam muito complexos para o banco de dados relacional tradicional. Auxilia a romper silos de dados e a obter insights preditivos e em tempo real sobre todos os dados com poucos cliques, sem migrar nem transformar dados.

Obtenha uma relação preço-performance até cinco vezes melhor do que qualquer outro data warehouse na nuvem, com inovação de performance pronta para uso, sem custo adicional. Extraia insights de dados em segundos sem se preocupar com o gerenciamento de infraestrutura, com um serviço de data warehouse seguro e confiável.

## DMS - Database Migration Service

Ele ajuda você a mover dados entre bancos de dados, utilizando um banco de dados de origem e um banco de dados de destino. Um banco de dados de origem é um banco de dados de onde os dados são migrados, um banco de dados de destino é um banco de dados para o qual os dados serão migrados.

Seu banco de dados de origem permanecerá operacional durante o processo de migração, sendo simples de usar, reduzindo o tempo de inatividade do aplicativo, oferecendo suporte a uma ampla gama de bancos de dados, com baixo custo e altamente confiável.

> Uso

- Ative o aplicativo de teste em relação aos dados de produção ou outros ambientes, sem afetá-los
- Combine vários bancos de dados em um único banco
- Envie seus dados para outras fontes de dados

## Serviços de banco de dados adicionais

Existem várias opções de banco de dados que a AWS fornece.

### AWS DocumentDB

O AWS DocumentDB é um serviço de banco de dados baseado em documentos, sendo um tipo de banco de dados NoSQL que suporta MongoDB. É ideal para sistemas de gerenciamento de conteúdo, perfis de usuários e catalogação.

### AWS Neptune

AWS Neptune é um serviço de banco de dados gráfico que pode ser usado para criar gráficos de seus dados para várias finalidades. É ótimo para registros financeiros, sistemas de cadeia de suprimentos e outros registros digitais centralizados.

> Uso

- Transforme a personalização com o Customer 360
- Detecte padrões de fraude
- Revele previsões de machine learning
- Aumente a segurança da TI

### AWS QLDB (Quantum Ledger Database)

AWS QLDB é um serviço de banco de dados contábil que fornece dados históricos de todas as alterações de seu aplicativo. É ótimo para registros financeiros, sistemas de cadeia de suprimentos e outros registros digitais centralizados.

> Vantagens

- Rastreie e mantenha um histórico sequencial de cada mudança de dados de aplicação utilizando um diário imutável e transparente
- Confie na integridade de seus dados. A verificação criptográfica integrada habilita a validação de mudança de dados por terceiros
- Construção correta, sistemas orientados por evento com transações QLDB ACID e compatibilidade com a transmissão em tempo real para a Amazon Kinesis
- Inicie de forma pequena e pague apenas pelo o que é utilizado com uma arquitetura sem servidor que fornece armazenamento automático e escalabilidade de recursos

> Uso

- Armazenamento de transações financeiras
- Reconcilie os sistemas de cadeia de suprimentos
- Mantenha o histórico de declarações
- Centralize os registros digitais

### AWS Managed Blockchain

AWS Managed Blockchain é um serviço que utiliza estruturas de código aberto para criar ou gerenciar redes blockchain. Com alguns cliques, você pode ingressar, criar e gerenciar redes blockchain. O Amazon Managed Blockchain é um serviço totalmente gerenciado que facilita o ingresso em redes públicas, cria e gerencia redes de blockchain privadas usando as conhecidas estruturas de código aberto Hyperledger Fabric e Ethereum.

> Vantagens

- Totalmente gerenciado
- Opções do Hyperledger Fabric ou do Ethereum
- Escalável e seguro
- Confiabilidade

> Uso

- Transferência de ativos e transações
- Varejo
- Cadeia de suprimentos

### AWS ElastiCache

O AWS ElastiCache adiciona camadas de captura sobre um banco de dados, a camada de captura armazena uma parte dos dados, acelerando o desempenho do aplicativo e melhorando os tempos de leitura das solicitações de banco de dados. Redis e Memcached são compatíveis com o serviço AWS ElastiCache.

> Vantagens

- Obtenha tempos de resposta de microssegundos em centenas de milhões de operações por segundo e até 1 pebibyte de dados (com hierarquização de dados)
- Obtenha 99,99% de SLA com implantações Multi-AZ e reforce a recuperação de desastres em menos de um minuto por meio da replicação entre regiões
- Obtenha uma performance otimizada ao adicionar um cache para dados lidos com frequência para aprimorar os recursos e reduzir o custo total de propriedade
- Construa aplicações rapidamente usando tecnologias populares de código aberto, Redis e Memcached, e integre-se facilmente com outros serviços da AWS

> Uso

- Redução do custo total de propriedade
- Cache de dados de aplicações em tempo real
- Armazenamentos de sessões em tempo real
- Classificações em tempo real