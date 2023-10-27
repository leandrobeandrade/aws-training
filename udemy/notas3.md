# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Outros Serviços

Outros serviços gerais indispensáveis para uso na AWS.

O **`Elastic Container Service (ECS)`** lança contêineres Docker na AWS, necessita das instâncias EC2 já estarem criadas e é integrado com ELB.

O **`Fargate`** é um serviço serverless utilizado para lançar contêineres na AWS, porém com Fargate não precisamos ter a infraestrutura (EC2) criada.

O **`Elastic Container Registry (ECR)`** é serviço que armazena imagens do Docker na AWS para serem utilizadas pelo ECS ou Fargate.

O **`Lambda`** é serviço serverless que fornece funções virtuais sem gerenciamento com limites de tempo para execuções curtas de até no máximo 15 minutos, sob demanda e automaticamente escalonadas. Os preços são baseados nas ligações e durações, benefícios:

- preço pago por uso, por request e free tier (1.000.000) e computação (400.000).
- integrado com vários outros serviços AWS e linguagens como Java, Python, Node...
- reativo só acontecendo quando um evento for acionado (Event-Driven).
- monitorado pelo CloudWatch.
- aumento de RAM que melhora de CPU e rede com até 10GB de RAM.

O **`Cron Job`** permite definir uma programação por períodos para executar determinada função Lambda, sendo executado por uma máquina Linux AMI.

O **`API Gateway`** é um serviço escalonável que permite a criação de um proxy de conexão sendo utilizado por exemplo para expor uma função Lambda ou outros serviços serverless para usuários externos. Altamente gerenciado e fornece criação, publicação, manutenção, monitoração e proteção de APIs na nuvem. Suporta protocolos Rest e WebSocket além de autenticações, limitação de chaves, etc...

O **`Batch`** é um serviço de processamento em lote em grande escala e com eficiência totalmente gerenciado. **Batch job** é uma funcionalidade com começo e fim, são imagens Docker e que rodam em um ECS. Provisiona dinamicamente a quantidade e o tipo ideais de recursos de computação (por exemplo, CPU ou instâncias com otimização de memória) com base no volume e nos requisitos de recursos específicos dos trabalhos em lote enviados.

O **`Lightsail`** é a junção de serviços AWS em um único lugar com preços baixos e previsíveis abstraindo as complexidades destes serviços. Podendo-se configurar recursos de notificações e monitoramento. Bom para frameworks como Nginx, MEAN, Node, Lamp e CRM's como Joomla, Magento, Plesk, Wordpress, **também para ambientes de desenvolvimento e testes**.

O **`CloudFormation`** é um forma declarativa de provisionar a infraestrutura através de código na AWS para quaisquer recursos gratuitamente. Cada recurso criado terá uma tag associada para facilmente estimar custos. Com criação e exclusão de recursos rapidamente e programaticamente, geração de diagramas automáticos,  com replicações para AZ's, regions e outras contas AWS.

O **`Cloud Development Kit (CDK)`** é maneira de definir infraestrutura na AWS utilizando uma linguagem familiar como Python, JavaScript, TypeScript, etc... depois o código é compilado para JSON ou YAML para ser utilizado no CloudFormation. Bom para funções Lambda e serviços Docker (ECS/EKS).

O **`Elastic Beanstalk`** fornece uma visão central para desenvolvedores implantarem um app na AWS sem precisar se preocupar com infraestrutura sendo uma plataforma PaaS gratuita. Fornece monitoramento de integridade e capacidade de resposta do app.

O **`System Manager (SSM)`** é um sistema gerenciador híbrido de instâncias EC2 e On-Premises em escala que fornece insights operacionais sobre todas estas infraestruturas através da instalação de um agente que roda em segundo plano em um computador. Controla os serviços por um shell seguro sem necessidade de chaves ssh, Http/Https ou porta 22.

O **`OpsWorks`** é um serviço alternativo ao SSM e trabalha em conjunto com as aplicações Chef e Puppet que realizam automatizações de configurações repetitivas no servidor.

A AWS fornece também uma suíte completa com serviços para todos os ciclos de vida de uma aplicação:  

- **CodeDeploy**: Faz entrega de apps atualizando as versões, funciona com instâncias EC2 e On-Premise Servers.
- **CodeCommit**: Parecido com Github é um serviço de armazenamento e controle de versões de código usando GIT.
- **CodeBuild**: Faz a compilação de códigos, execução dos testes e entrega dos pacotes para implantação, pago por tempo de uso.
- **CodePipeline**: Define os passos a serem executados para a entrega de código - code -> build -> test -> staging -> production.
- **CodeArtifact**: Armazena e recupera dependências utilizadas nos apps.
- **CodeStar**: Interface gráfica que envolve todos os outros serviços de códigos.
- **Cloud9**: IDE online para fazer todo o processo de desenvolvimento na própria plataforma AWS.

## Infraestrutura Global AWS

A Infraestrura AWS é formada por:

- Data centers: local físico que armazena máquinas de computação e seus equipamentos de hardware relacionados.
- Regions: local físico em todo o mundo onde agrupamos data centers.
- AZ's: um ou mais data centers distintos com energia, rede e conectividade redundantes em uma região da AWS.
- Edge Locations (Locais de borda): pontos de presença que o CloudFront usa para armazenar cópias do seu conteúdo em cache para entrega mais rápida aos usuários em qualquer local.

Aplicações se tornam globais através da infraestrutra da AWS que promove baixa latência, recuperação de desastres e proteção contra ataques, otimizando a velocidade das aplicações em até 60%.

O **`Route 53`** é um DNS gerenciador de domínios AWS, ele envia para o cliente um ip que é o endereço do servidor, o cliente faz a requisição ao ip indicado e o servidor envia a resposta de volta ao cliente. Possui políticas de roteamento sendo a `Simples`, a `Ponderado` que distribui tráfego por instâncias em medidas proporcionais, a `Latência` que distribui tráfego por regions e a `Failover` que verifica a saúde das instâncias e faz o direcionamento para a melhor. Fora a primeira todas possuem verificações de saúde.

O **`CloudFront`** fornece uma rede de entrega de conteúdo **(CDN)** que melhora o desempenho armazenando em cache os conteúdos dos sites, estando presente em 216 Edge Locations. Conecta-se a S3, EC2, ELB, Http, etc... Armazena conteúdo em todo mundo enquanto a replicação S3 transversal replica o bucket inteiro em outra region. Possui o OAC Origin Access Control.

O **`S3 Transfer Acceleration`** transfere arquivos de um bucket de um edge location para outro bucket por meio de um caminho de rede otimizado.

O **`Global Accelerator`** não armazena em cache, as solicitações são repassadas dos edge locations para os apps nas regions.

O **`Outposts`**  são racks de servidores AWS fora da AWS, no data center do cliente com os serviços disponíveis configurados. Sendo o cliente responsável pela segurança em todos os aspectos.

O **`WavesLength`** são data centers de provedores de telecomunicações na bordas das redes 5G.

O **`Local zones`** estende os VPC's para zonas distintas, é uma espécie de implantação de infraestrutura que posiciona a computação, armazenamento, banco de dados e outros produtos seletos da AWS perto do público em geral e dos centros industriais. Presente apenas nos EUA.

## Cloud Integrations

A integração de aplicativos na AWS é um conjunto de serviços que permite a comunicação entre componentes desacoplados em microsserviços, sistemas distribuídos e aplicativos sem servidor.

O **`Simple Queue Service (SQS)`** permite receber mensagens de vários produtores e armazenadas em fila (FIFO) para serem consumidas de forma compartilhada pelos consumidores. Desacopla aplicativos e é serverless, retém mensagens por 4 dias por padrão e no máximo por 14 dias.

O **`Kinesis`** é um Streaming de big data em real time com baixa latência. Possui 4 serviços Data Firehose, Data Analytics, Data Streams, Video Streams.

O **`Simple Notification Service (SNS)`** publica notificações para um tópico SNS e os inscritos ouvem todas essas notificações.

O **`AWS MQ`** trabalha em conjunto com RabbitMQ e ActiveMQ para quem não quiser os outros serviços de mensagens AWS. Utilizado muito em migrações para nuvem para manter a compatibilidade com o que já estava funcionando (protocolos MQTT, AMQP).

## Cloud Monitoring

O monitoramento da AWS verifica seus recursos e aplicativos da AWS, coletando dados para garantir que tudo esteja funcionando de maneira tranquila e segura. O monitoramento da infraestrutura da AWS ajuda a identificar vulnerabilidades e problemas, prever o desempenho e otimizar configurações.

O **`CloudWatch`** fornece métricas (variáveis monitoradas) para os serviços AWS. Exemplos: utilizações de CPU, status check, network em EC2 (por padrão a cada 5 minutos), leitura/escrita em volumes EBS, requests, NumberOfObjects em buckets S3, limite de serviços, etc...

O **`AWS Alarms`** dispara notificações para qualquer métrica por períodos definidos. Exemplos: auto scaling, stop, terminate, reboot ou recover em instâncias EC2, notificações SNS, etc... Tem os estados OK, Insufficient_Data e Alarm.

O **`Logs`** coleta logs de diversos serviços AWS como Elastic Beanstalk, ECS, Lambda, CloudTrail, Route 53 (logs de DNS queries).

O **`EventBridge`** reage a eventos dentro da conta AWS, agenda jobs no Cron, emite notificações com SNS por tentativas de login com root user, aciona funções Lambda, entre outros.

O **`CoudTrail`** fornece governança, conformidade e auditoria com histórico de todas as chamadas as API's ou eventos na AWS.

O **`X-Ray`** rastreia e analisa visualmente as aplicações, utilizado para realizar troubleshootings, comportamentos de solicitações, velocidade, etc... Também ajuda os desenvolvedores a analisar e depurar aplicações distribuídas de produção, como aquelas criadas usando uma arquitetura de microsserviços.

O **`CodeGuru`** é baseado em aprendizado de máquina, faz code reviews automatizados e recomendações de desempenho de apps. Trabalha em conjunto do Git, Bitbucket, CodeCommit.

O **`AWS Health Dashboard`**  mostra a saúde dos serviços em todas as regions (contas geral AWS), fornece alertas e orientações de remediação que impactaram a nossa conta (conta específica).
