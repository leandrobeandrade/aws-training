# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Gerenciamento de contas, faturamento e suporte

A AWS fornece uma visão geral e completa para o gerenciamento de contas, para o faturamento de custos, assim também como um serviço de suporte que cobre todos os níveis de necessidades dos seus clientes.

> Gerenciamento de contas AWS

O **`Organizations`** é um serviço global que gerencia múltiplas contas dentro da AWS, a principal é a mestra e a derivadas são contas-filho. Fornece faturamento consolidado, ou seja, todas as contas derivadas são pagas pela mestra ganhando desconto pelo uso no agregado (em lote) dos serviços e facilita pois só é gerado 1 fatura, também fornece API para automatizar a criação de contas-filho assim como a Control Tower com um painel interativo de fácil gerenciamento. Restringe privilégios de contas facilmente por SCP's. Extensão de várias VPC's através de 1 conta para as contas-filho, uso de tagueamento para detalhes de faturamento, usar CloudTrail em todas as contas com logs enviados para um S3 e CloudWatch na conta mestra.

O **`Service Control Policies (SCP)`** permite o uso de listas de permissões ou negações de IAM aplicadas no nível de contas-filho ou unidade organizacional(OU) para usuários e funções que por padrão são criadas sem nenhuma permissão.

O **`Control Tower`** fornece uma maneira fácil de configurar e administrar um ambiente AWS de forma segura e compatível com várias contas, automatizando as configurações dos ambientes AWS em poucos cliques e o gerenciamento contínuo de políticas utilizando grades de proteção.

O **`Resource Access Manager (RAM)`** permite o compartilhamento de recursos entre contas AWS.

O **`Catalog`** é um portfólio de produtos AWS que podem ser utilizados pela conta.

> Faturamento

O Modelo de preços da AWS fornece alguns tipos que se adequam para cada necessidade em específico. 

- `pay-as-you-go`: pago pelo uso com agilidade de iniciar, interromper e excluir serviços sob demanda.
- `save when you reserve`: economia ao reservar minimizando riscos com orçamento previsível a longo prazo para EC2, DynamoDB, ElastiCache, RDS e Redshift.
- `pay less by using more`: descontos baseado no volume de uso, quanto mais uso, maior será o desconto.
- `pay less as AWS grows`: quanto mais pessoas usando, mais a infraestrutura aumenta e consequentemente os serviços terão mais descontos.

A AWS fornece alguns serviços grátis em alguns níveis dependendo do local como AIM, VPC, Conta consolidada, já o Elastic Beanstalk, CloudFormation e o Auto Scaling Groups paga-se pelos recursos criados.

O EC2 possui os seguintes tipos de preços: 

- **On-demand** - sob demanda com tempo mínimo de faturamento de 60s e pago por segundo ou por hora. 
- **Instâncias reservadas** - 75% de desconto em relação a on-demand por hora, com comprometimento de 1 ou 3 anos podendo pagar tudo adiantado com desconto ou reembolsos. 
- **Instâncias Spot** - 90% de desconto em relação a on-demand por hora, com lances para as capacidades não usadas.
- **Host dedicado** - pode-se utilizar com on-demand ou instância reservada de 1 ou 3 anos.
- **Saving Plans** - o cliente compromete-se a gastar uma certa quantia em dólares por hora durante 1 ou 3 anos sem a necessidade de pensar nos recursos mas sim em termos somente do custo. Com este modelo para instância EC2 obtém-se 72% de desconto em relação a on-demand podendo pagar adiantado e para Computação Cloud são chamados de plano poupança de computação com 66% de desconto em relação a on-demand.

O **`Compute Optimizer`** recomenda recursos ideais para suas cargas de trabalho, a fim de reduzir custos e melhorar o desempenho usando machine learning para analisar métricas de históricos de utilização. Funciona para instâncias EC2, Lambda Functions e EBS (Elastic Block Store). 

O **`Pricing Calculator`** é uma calculadora que serve para estimar preços de serviços AWS.

O **`Billing Dashboard`** é um serviço para rastrear custos entre contas AWS.

O **`Cost Allocation Tags`** é utilizado para rastrear custos em um nível detalhado e agrupado.

O **`Cost and Usage Reports`** é utilizado para rastrear custos gerando relatórios com conjunto abrangente de dados, pode ser integrado com Athena, Redshift ou QuickSight.

O **`Cost Explorer`** rastreia o custo total das contas ao longo do tempo, fornece relatórios mensais, por hora ou por recurso, prevendo custos de até 12 meses em comparação com custos anteriores.

O **`Billing Alarms`** fornece métricas de faturamento armazenadas no CloudWatch em 1 região, tendo os dados agregados para todas as regiões em uso e corresponde ao custo real e não ao custo projetado, podendo criar os alarmes em cima das métricas de faturamento.

O **`Budgets`** gera alarmes quando os custos excedem ao limite, são 4 tipos: Usage, Cost, Reservation e Saving Plans. Os 2 primeiros são grátis, os outros custam $0.02 dia.

O **`Anomaly Detection`** monitora continuamente os custos e uso, utilizando Machine Learning para detecções.

O **`Service Quotas`** cria alarmes em conjunto com CloudWatch para alertas sobre limites ultrapassados.

O **`Trusted Advisor`** executa uma série de verificações analisando as contas fornecendo recomendações sobre tempo de otimização de custos, desempenho, segurança, tolerância a falhas e limite de serviços. Verificações planos `Básico/Developer`: permissões S3, SG (algumas portas), IAM Use, MFA (na conta raíz), EBS com snapshots públicos, RDS, limites de serviços. Verificações planos `Business/Enterprise` todas dos planos básicos/developer mais alarmes CloudWatch ao atingir limites e acesso programático usando AWS Support API.

> Suporte

A AWS fornece alguns tipos de planos de suporte que satisfaz cada necessidade.

- **Basic Plan**: gratuito com suporte 24/7, documentações, whitepapers e a fóruns de suporte.
- **Developer Plan**: plano básico mais acesso ao e-mail Cloud Support Associates e orientações gerais dentro de 24 horas e problemas no sistema contato em 12 horas.
- **Business Plan**: planos anteriores mais telefone, e-mail e chat para contato imediato com o suporte e acesso de gerenciamento de eventos de infraestrutura por uma taxa adicional.
- **Enterprise Plan**: planos anteriores mais pool de gerentes técnicos (TAM - Technical Account Manager), além de Concierge Support Team para boas práticas sobre contas e análises de operações.

## Demais serviços

Serviços não tão usuais mas que complementão o portfólio AWS na nuvem.

O **`WorkSpaces`**  é um desktop gerenciado como serviço, provisionando Windows ou Linux, fornece VDI (Virtual Desktop Infrastructure) rapidamente e facilmente com segurança, pago pelo uso diminuindo a latência.

O **`AppStream 2.0`** é um serviço stream de aplicativos desktop com acessos sendo fornecidos pelo browser sem conexão com uma VDI.

O **`IoT Core`** são dispositivos que coletam e transferem dados, sendo serverless, escalonável e seguro mesmo offline, conectando bilhões de dispositivos.

O **`Elastic Transcoder`** converte arquivos de mídia armazenados na AWS em arquivos no formato desejado para tablets, smartphones, pc's, trabalha em conjunto com S3 e pago pelo uso.

O **`AppSync`** fornece um back-end para aplicações web e mobile em tempo real utilizando GraphQL em conjunto com Lambda e DynamoDB.

O **`Amplify`** fornece uma suíte completa para gerenciamento de aplicações web e mobile.

O **`Device Farm`** fornece testes sincronizados para aplicações web e mobile em diversos dispositivos, celulares, tablets e browsers.

O **`AWS Backup`** fornece gerenciamento automatizado centralizado de backups sob demanda e agendados com suporte para recuperação pontual (PITR) em regions ou entre contas AWS.

O **`Elastic Disaster Recovery`** permite a recuperação rápida e fácil de servidores virtuais.

O **`CloudEndure Disaster Recovery`** minimiza o tempo de inatividade e a perda de dados, fornecendo recuperação rápida e confiável na AWS de seus servidores físicos, virtuais e baseados em nuvem.

O **`DataSync`** move grande quantidade de dados on-premises para a nuvem AWS com testes de replicação.

O **`Application Discovery Service`** mapeia os dados e as dependências para a migração de on-premises para a AWS, com 2 tipos de migrações o A`gentless Discovery` que utiliza um conector dando informações sobre máquinas virtuais, configurações, CPU, memória e disco rígido e o `Agent-based Dicovery` com mais informações e atualizações gerais. Ambas migrações podem ser visualizadas pelo AWS Migration Hub.

O **`Application Migration Service`** converte servidores físicos, virtuais e baseados na nuvem para a AWS.

O **`Migration Evaluator`** auxilia na criação de um caso de uso orientado a negócios para migração instalando o coletor sem agente.

O **`Fault Injection Simulator (FIS)`** executa testes de falhas baseado em engenharia do caos com promoção de cargas de estresse para as aplicações.

O **`Step Functions`** constrói um fluxo de trabalho visual (diagrama) serverless para orquestrações de funções Lambdas.

O **`Ground Station`** permite controlar comunicação e dimensionar operações via satélite e assim processar dados do tipo previsão meteorológicas, geolocalizações, etc...

O **`AWS Pinpoint`** serviço escalável de 2 maneiras (entrada e saída) para comunicação de marketing em massa, segmentando e personalizando mensagens de texto, SMS, e-mail, etc... para clientes.
