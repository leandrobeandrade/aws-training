# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Escalabilidade, disponibilidade e elasticidade

A escalabilidade e alta disponibilidade dão o poder de cargas maiores de trabalho por meio de adaptação.

- **escalabilidade vertical:** pode aumentar o tamanho da instância, tendo a limitação de hardware.
- **escalabilidade horizontal:** também conhecida como `elasticidade`, pode aumentar o número de instâncias e utiliza **Auto Scaling Group** e **Load Balancer**.
- **alta disponibilidade:** execução de aplicativos em pelo menos 2 AZ's.

O **`Elastic Load Balancer (ELB)`** é um servidor de carga que encaminha o tráfego da internet para vários servidores (Instâncias EC2). Expõe um único ponto de acesso (DNS). Checa a saúde das instâncias e fornece terminação SSL (HTTPS) para sites, tornando as aplicações altamente disponíveis para múltiplas AZ's.

Tipos de ELB:

- `ALB (Aplication Load Balance):` Http/Https/gRPC com protocolos da camada 7, recursos de roteamento e DNS estático.
- `NLB (Network Load Balance):` TCP/UDP com protocolos da camada 4, alto desempenho e fornece IP estático ao invés de uma UUL estática.
- `GLB (Gateway Load Balance):` GENEVE com protocolo da camada 3, examina e encaminha o tráfego para um firewall de uma instância EC2.

O **`Auto Scaling Group (ASG)`** escala horizontalmente podendo criar e excluir rapidamente servidores (instâncias EC2) apenas do mesmo tipo, executar o máximo e o mínimo de máquinas com enorme economia de custos trabalhando em conjunto com um ELB.

Estratégias ASG:

- Escalabilidade manual.
- Dimensionamento dinâmico para responder as demandas de mudanças com CloudWatch e TTS (Target Tracking Scaling).
- Escalonamento agendado que antecipa o escalonamento baseado em alguns padrões.
- Escalonamento preditivo que utiliza aprendizado de máquina para prever o tráfego futuro.

## S3

Armazenamento em escala infinita, utilizado também para fazer integrações entre outro serviços AWS. Armazenamento de arquivos, recuperação de desastres, nuvem híbrida, hospedar apps e sites, analisar dados, fornecer atualizações de softwares. O armazenamento é realizado em `Buckets` que devem ter nomes únicos globalmente e podem ser distribuídos em várias regions. Os dados armazenados são conhecidos como **Objects** com tamanho máximo 5 TB (5000GB) e possuem uma key que é o caminho para o arquivo.

As políticas de segurança dos buckets (Buckets Security Policies) são por meio de IAM com um documento do tipo **JSON** que garante acesso específico por usuário ou por outro serviços (Roles), também pode garantir acesso por cruzamento de contas, por ACL's, assim também como por meio de criptografia. Políticas:

- effect: permitir/negar (allow/deny)
- actions: conjunto de API para permitir/negar (S3:GetObject por exemplo)
- principal: usuário/conta que se aplica a regra (* - todos por exemplo)
- resource: o recurso a ser aplicado a regra (arn:aws:s3:::examplebucket/* por exemplo)

O **S3 Replication** consiste na replicação de um bucket sendo que o CRR (Cross-Region Replication) replica o bucket em outras regions e o SRR (Same-Region Replication) replica na mesma region, todos de forma assíncronas.

### S3 - Classes

Na criação do Bucket pode-se escolher a classe, modificar manualmente e utilizar o ciclo de vida. Com durabilidade dos dados de **99,999...(onze 9's)** entre AZ's, perde-se apenas 1 objeto entre 10 milhões a cada 10 mil anos isso para qualquer classe. Com disponibilidade de **99,99%** (53 minutos fora em 1 ano). Classes:

- **General Purpose**: 99,99 disponibilidade, uso frequente, baixa latência e altas taxas de transferência. Uso - Big Data, gaming, distribuição de conteúdo.
- **Infrequent Access**: 99,9 disponibilidade e dados pouco acessados, mas imediato quando necessário. Uso - Backups e recuperação de desastres.
- **One Zone-IA**: 99,5 disponibilidade e 99,99...(nove 9's) durabilidade em uma única AZ, que se perdida os dados também são. Uso - Backups secundários de dados locais ou recriados.
- **Glacier**: Baixo custo dedicado a armazenamento e backups, custando armazenamento + recuperação.
    - Instant Retrieval: recuperação em milisegundos e bom para dados acessados por trimestre com mínimo de 90 dias de armazenamento.
    - Flexible Retrieval:  custoso (expendit) recuperação de 1/5 minutos, padrão (standard) 3/5 horas e volumoso (bulk) de 5/12 horas e grátis e com mínimo de 90 dias.
    - Deep Archive: longo prazo com camadas standard de 12 horas e bulk de 48 horas de recuperação. Menor custo e mínimo armazenamento de 180 dias.
- **Intelligent-Tiering**: Permite mover camadas em excesso com base em padrões pagando-se por uma pequena taxa mensal de monitoramento e classificação automática sem cobranças de recuperação.
    - Frequent Access tier: automático e padrão.
    - Infrequent Access tier: automático e objetos não acessados por 30 dias.
    - Archive Instant Access tier: automático e não acessados por 90 dias.
    - Archive Access tier: opcional e configurável de 90 a mais de 700 dias.
    - Deep Archive Access tier: opcional e configurável de 180 a mais de 700 dias.

### S3 - Snow Family

Dispositivos para armazenamento de dados, pode-se utilizar com a interface gráfica **`OpsHub`**.

- **`Snowcone e Snowcone SSD`:** capacidade de armazenamento 8TB HDD e 14TB SSD, recomendado para pequenos volumes de dados e locais de borda. funciona enviando o dispositivo físico para a AWS ou enviando os dados por uma rede (DataSync).
- **`Snowball Edge`:** 80TB HDD (Storage Optmized) 42TB HDD ou 28TB VNMe (Compute Optimized), recomendado para grandes armazenamentos e backups volumosos de dados e recuperação de desastres.
- **`Snowmobile`:** armazenamento de 100PB por um caminhão, temperatura controlada, GPS e segurança. Menos que 10PB utilizar Snowball Edge.

A **computação de borda (Edge Computing)** permite uma computação remota, sem ou com pouco acesso a internet, a infra e a recursos computacionais. Esta computação de borda pode ser utilizada com **Storage Gateway** que serve como uma ponte de conexão entre armazenamento local e a nuvem (cloud híbrida), utilizado para recuperação de dados, backups e restaurações. Possui 3 tipos files, volumes e tapes.

## Banco de Dados

A AWS oferece bancos de dados na nuvem, banco de dados NoSQL, serviço de data warehouse e cache na memória de acordo com cada necessidade específica.

- Relational Database Service
> Utiliza SQL com gerenciamento para bancos PostgreSQL, MySQL, MariaDB, Oracle, Microsoft SQL Server. Utilizado para transações OLTP. O objetivo principal das implantações RDS Multi-AZ é a alta disponibilidade, enquanto o objetivo principal das réplicas RDS Read é a escalabilidade.
- Aurora
> Simula e gerencia bancos PostgreSQL 3x mais performático que no RDS e 5x mais que MySQL no RDS. Expande de 10GB até 128TB, mesmo custando 20% a mais que RDS há economia pela performance melhor.
- ElasticCache
> Gerenciador Redis ou memCached, banco de dados na memória com alto desempenho e baixa latência reduzindo cargas sobre o banco.
- DynamoDB
> Totalmente gerenciado e altamente disponível com replicação em 3 AZ's e NoSQL para cargas massivas com desempenho rápido e consistente e sem servidor distribuído (Serverless) apesar dos servidores existirem no back-end porém ficam ocultos. Baixo custo e recursos de dimensionamento automático e integrado com IAM para segurança e autorização.
- DAX ou DynamoDB Accelerator
> É um cache de memória gerenciado pelo DynamoDB,  sendo 10x mais rápido do que com o acesso direto ao DynamoDB.
- Redshift
> É baseado em PostgreSQL não é para uso OLTP, mas sim OLAP (Online Analytical Processing) e data warehousing. Os dados são armazenados em formato de colunas e não linhas e são carregados uma vez a cada 1 hora com desempenho 10x melhor que outros data warehouses, podendo ser dimensionado para petabytes. Pago pelo uso, com fácil integração a BI como AWS Quicksight ou Tableau.
- EMR Elastic MapReduce
> É utilizado com clusters Hadoop, provisiona todas as instâncias EC2 e configura-as para funcionar juntas e fazer análises de dados e big data. Integrado com instâncias Spot com escalonamento automático.
- Athena
> Serviço de consulta serverless para análises relacionadas a objetos S3. Serve para análises, BI ELB logs, relatórios, etc... com custo de 5$ por TB.
- QuickSight
> Serviço serverless escalonável de BI baseado em aprendizado de máquina para criar painéis interativos.
- DocumentDB
> Simula MongoDB na AWS sendo NoSQL utilizado para armazenar, consultar e indexar dados JSON, sendo altamente gerenciado, disponível por 3 AZ's e escalonado automaticamente de 10GB até 64TB.
- Neptune
> Banco de dados gráfico totalmente gerenciado recomendado para rede sociais por exemplo. Replicação em 3 AZ's com alta disponibilidade para realizar consultas a dados relacionados entre si.
- Quantum Ledger DataBase
> Espécie de livro-razão como banco de dados que registra transações financeiras e históricos de mudanças, serverless altamente gerenciado e disponível replicado em 3 AZ's. Dados imutáveis que podem ser criptografados, 2 ou 3x mais performático que blockchains e pode manipular dados SQL. Sendo apenas um único banco centralizado.
- Blockchain
> Permite monitorar aplicações com transações simultâneas descentralizadas compatível com Hyperledger Fabric e Ethereum.
- Glue
> Serviço serverless gerenciado de extração, transformação e carregamento (ETL) de dados. Utilizado para facilitar a formatação dos dados para análises em outros serviços como Redshift. Com o Glue Data Catalog podemos definir campos, nomes etc.. para fazer as transformações.
- DMS - Database Migration Service
> Fornece migrações rápidas, seguras, autocorretivas e resiliente entre bancos. Com migração homogênea entre bancos do mesmo tipo e heterogêneas com tecnologias diferentes.
