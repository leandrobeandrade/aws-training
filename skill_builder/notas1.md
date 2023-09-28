# AWS - Anotações gerais

Anotações referentes ao curso [AWS Cloud Practitioner Essentials](https://explore.skillbuilder.aws/learn/course/8287/elementos-essenciais-do-aws-cloud-practitioner-portugues-aws-cloud-practitioner-essentials-portuguese) na plataforma AWS Skill Builder.

## Vantagens da nuvem AWS

Operar na nuvem AWS oferece muitos benefícios em relação à computação em ambientes locais ou híbridos.

- Trocar despesa antecipada por despesas variáveis

Despesas iniciais são data centers, servidores físicos e outros recursos nos quais você precisaria investir antes de usá-los. Em vez de investir substancialmente em datacenters e servidores antes de saber como serão usados, você pode pagar somente ao consumir recursos de computação.

- Benefícios de enormes economias de escala

Com a computação em nuvem, é possível obter um custo variável inferior ao do seu ambiente local. Como o uso por centenas de milhares de clientes se acumula na nuvem, provedores como a AWS podem alcançar economias de escala maiores. As economias de escala se transformam em preços para pagamento conforme usos mais baixos.

- Parar de tentar adivinhar a capacidade

Com a computação em nuvem, você não precisa prever a capacidade de infraestrutura necessária antes de implantar um aplicativo. Por exemplo, você pode iniciar instâncias do AWS EC2 quando necessário e pagar apenas pelo tempo de computação usado. Em vez de pagar por recursos que não são utilizados ou lidar com capacidade limitada, você pode acessar somente a capacidade de que precisa e aumentar ou reduzir a quantidade em resposta à demanda.

- Aumentar a velocidade e a agilidade

A flexibilidade da computação em nuvem facilita o desenvolvimento e a implantação de aplicativos. Essa flexibilidade também oferece às suas equipes de desenvolvimento mais tempo para experimentar e inovar.

- Parar de gastar dinheiro com execução e manutenção de data centers

A computação em nuvem em data centers geralmente exige que você gaste mais dinheiro e tempo gerenciando infraestrutura e servidores. Um benefício da computação em nuvem é poder se concentrar menos nessas tarefas e mais em seus aplicativos e clientes.

- Ter alcance global em minutos

O espaço global da nuvem AWS para implantação rápida de aplicativos para clientes em todo o mundo, ao mesmo tempo em que oferece baixa latência.

## Modelos de implantação

- Baseada na nuvem: soluções totalmente baseadas em nuvem como servidores virtuais, banco de dados, componentes de rede, etc...
- Implantação local: ou nuvem privada `(On-premises)` mantém tudo dentro das instalações da sua organização.
- Implantação híbrida: ou `(Outposts)` combina recursos locais com serviços em nuvem da AWS para oferecer flexibilidade e escalabilidade adicionais, como virtualização.

Sendo a computação em nuvem o "fornecimento sob demanda de recursos e aplicativos de TI pela internet com modelo de pagamento conforme o uso". 

## EC2 - Elastic Compute Cloud

Servidores virtuais elásticos que aumentam ou diminuem sua capacidade conforme a demanda configurada.

### Tipos de instâncis EC2

> Uso geral

    Equilibram os recursos de computação, memória e rede.

> Otimizadas para computação

    Executam sob processadores de alto desempenho, ideais para servidores web de alto desempenho, servidores de aplicativos
    de computação intensiva e de jogos dedicados.

> Otimizadas para memória

    Ideais para cargas de trabalho que processam grandes conjuntos de dados na memória, como exemplo um banco de dados.

> Computação acelerada

    Utilizam aceleradores de hardware ou coprocessadores sendo ideais para aplicativos gráficos e streaming de jogos.

> Otimizadas para armazenamento

    Utilizadas em cargas de trabalho que demandam alto acesso sequencial de leitura e gravação a grandes conjuntos de dados.
    São ideais para aplicativos de data warehouse, sistemas de arquivos distribuídos e de processamento de transações(OLTP).

### Preços EC2

> **Sob demanda**

    Ideais para cargas de trabalho irregulares de curto prazo que não podem ser interrompidas. Custos antecipados ou 
    contratos mínimos não se aplicam.

> **Saving plans**

    Compromisso com uma quantidade consistente de uso por um período de 1 ou 3 anos, resultando em economias de até 72%
    em relação aos custos sob demanda.

> **Instâncias reservadas**

    São um desconto aplicado ao uso de instâncias sob demanda, podendo adquirir instâncias reservadas comuns ou conversíveis
    por um período de 1 ou 3 anos.

> **Instâncias spot**

    Ideais para cargas de trabalho flexíveis ou que toleram interrupções, usam a capacidade de computação nao utilizada do
    EC2 com economia de até 90% em relação aos custos sob demanda.

> **Hosts dedicados**

    Servidores físicos com capacidade totalmente dedicada ao uso, utilizando licenças de software por soquete, núcleo ou VM
    existentes para manutenção da conformidade. Podendo adquirir hosts sob demanda e hosts sob reservas. São os mais caros.

### Scaling

A escalabilidade envolve começar apenas com os recursos de que você precisa e projetar sua arquitetura para responder automaticamente às alterações de demanda, fazendo aumentos ou reduções. Como resultado, você paga apenas pelos recursos que usa.

### Auto Scaling

O Amazon EC2 Auto Scaling permite que você adicione ou remova automaticamente instâncias do Amazon EC2 em resposta à alteração da demanda do aplicativo. Ao fazer auto scaling de suas instâncias, aumentando ou reduzindo conforme a necessidade, você consegue manter uma maior disponibilidade de aplicativos.

No Amazon EC2 Auto Scaling, há duas abordagens disponíveis: scaling dinâmico e scaling preditivo. O scaling dinâmico responde às alterações na demanda. 
O scaling preditivo programa automaticamente o número correto de instância do Amazon EC2 com base na demanda prevista.

Em resumo com o Auto Scaling podemos definir uma capacidade mínima, uma capacidade desejada que se não definida será a mesma que a mínima e por fim uma capacidade máxima de instâncias EC2 AWS.

### ELB - Elastic Load Balance

Um balanceador de carga é uma aplicação que recebe requisições e faz o encaminhamento para processamento nas respectivas instâncias, é o serviço AWS que distribui automaticamente o tráfego de entrada de aplicativos entre vários recursos trabalhando em conjunto com o Auto Scaling.

Atua como um ponto único de contato para todo o tráfego da web de entrada no seu grupo do Auto Scaling. Isso significa que, à medida que você adiciona ou remove instâncias do Amazon EC2 em resposta à quantidade de tráfego de entrada, essas solicitações são direcionadas para o balanceador de carga primeiro.

## Messages

Mensagens estão relacionadas ao nível de acoplamento entre os serviços como instâncias EC2 por exemplo. Se um serviço A envia mensagens para o serviço B e este tem algum problema o serviço A também terá algum tipo de problema, isso é conhecido como alto acoplamento. Uma arquitetura tem um acoplamento mais flexível ou desacoplado quando um serviço A falha e não causa um efeito cascata de falhas em outros serviços. Para isso a AWS fornece os serviços SQS e SNS.

### SQS - Simple Queue Service

Serviço de enfileiramento de mensagens, envia, armazena e recebe mensagens sem perca. Um aplicativo envia mensagens para uma fila, um usuário ou serviço recupera a mensagem da fila, processa-a e a exclui da fila.

### SNS - Simple Notification Service

Serviço de pub/sub (publicação/assinatura) que consiste em um editor publicando mensagens que podem ser separadas por tópicos para os assinantes que podem ser servidores web, endereços de e-mail, funções Lambda, etc...

## Serverless

Termo que significa que o código é executado em servidores na nuvem sem qualquer provisionamento ou gerenciamento destes servidores, proporcionando uma flexibilidade em dimensionar aplicativos, ajustado-se automaticamente a capacidade e unidades de consumo como taxa de transferência e memória. Um exemplo de serviço serverless é o Lambda.

### AWS Lambda

Serviço que permite a execução de códigos sem a necessidade de provisionar ou gerenciar os servidores. Pagando apenas pelo uso durante o tempo que o código é executado, execução esta que é acionada por meio de um trigger ou origem de evento como serviços AWS diversos, aplicativos móveis ou endpoints Http.

### AWS Fargate

Mecanismo de computação serverless para contêineres funciona para orquestração de contêineres e trabalha em conjunto com ECS e EKS.

## Contêineres

Serviços de orquestração são comuns para empacotamento de códigos, configurações de dependências de um aplicativo em um único objeto, processos e fluxo com requisitos de segurança, confiabilidade e escalabilidade.

- **ECS - Elastic Container Service**

      Sistema de gerenciamento de contêineres altamente dimensionável e de alto desempenho e totalmente compatível com Docker.

- **EKS - Elastic Kubernetes Service**

      Serviço de gerenciamento completo para o Kubernetes na AWS, implantando e gerenciando aplicativos em grande escala.
