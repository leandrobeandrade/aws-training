# ECS - Elastic Container Service

O ECS ajuda você a executar aplicativos em contêineres. É um sistema de gestão construído para escala e alto desempenho.

## Vantagens

- Execute contêineres na AWS em grande escala sem se preocupar com a infraestrutura subjacente
- Reduza os custos com ajuste de escala automático e preço conforme o uso em várias opções de computação da AWS
- Implemente com mais rapidez e concentre-se em suas aplicações usando o Amazon ECS com a computação com tecnologia sem servidor do AWS Fargate para contêineres
- Crie no Amazon ECS com confiança, sabendo que a segurança, a conformidade e a arquitetura atendem aos padrões regulatórios

## Como funciona

O Amazon Elastic Container Service (Amazon ECS) é um serviço de orquestração de contêineres totalmente gerenciado que simplifica a implantação, o gerenciamento e a escalabilidade de aplicações conteinerizadas. Basta descrever suas aplicação e os recursos necessários, e o Amazon ECS vai executar, monitorar e escalar a aplicação em opções flexíveis de computação com integrações automáticas com outros serviços de suporte da AWS de que sua aplicação precise. Execute operações do sistema, como criar regras personalizadas de escalabilidade e capacidade, além de observar e consultar dados de logs de aplicações e telemetria.

É um serviço totalmente gerenciado de orquestração de contêineres ajuda a implantar, gerenciar e dimensionar facilmente aplicações conteinerizadas. Como um serviço totalmente gerenciado, o Amazon ECS vem com práticas recomendadas operacionais e de configuração da AWS incorporadas. Ele é integrado à AWS e a ferramentas de terceiros, como o Amazon Elastic Container Registry e o Docker. Essa integração torna mais fácil para as equipes se concentrarem na criação das aplicações, não no ambiente. Você pode executar e dimensionar suas workloads de contêiner Regiões da AWS em na nuvem e on-premises, sem a complexidade de gerenciar um ambiente de gerenciamento.

## Camadas ECS:

- Capacidade - A infraestrutura em que seus contêineres funcionam
- Controlador - Implante e gerencie seus aplicativos que são executados nos contêineres
- Provisionamento - As ferramentas que você pode usar para interagir com o agendador para implantar e gerenciar seus aplicativos e contêineres

> Capacidade do Amazon ECS

A capacidade do Amazon ECS é a infraestrutura em que seus contêineres são executados. Veja abaixo uma visão geral das opções de capacidade:

- Instâncias do Amazon EC2 na nuvem AWS
- Você escolhe o tipo de instância, o número de instâncias e gerencia a capacidade
- Sem servidor (AWS Fargate (Fargate)) na nuvem AWS
            
      - O Fargate é um mecanismo de computação sem servidor. 
      - pay-as-you-go.
      - Lidar com o planejamento de capacidade ou isolar workloads de contêiner para segurança.

- Máquinas virtuais (VM) ou servidores locais

      - O Amazon ECS Anywhere fornece suporte para registrar uma instância externa.
      - como um servidor on-premises ou uma máquina virtual (VM), no cluster do Amazon ECS.

A capacidade pode estar localizada em qualquer um dos seguintes AWS recursos:

- Uma VPC com zonas de disponibilidade e uma zona Wavelength
- Local Zones
- Zonas do Wavelength
- Regiões da AWS
- AWS Outposts
- Controlador Am

> Provisionamento do Amazon ECS

Há várias opções para provisionar o Amazon ECS:

- **AWS Management Console** - fornece uma interface da Web que você pode usar para acessar seus recursos do Amazon ECS.

- **AWS Command Line Interface (AWS CLI)** - fornece comandos para um amplo conjunto de serviços da AWS, incluindo o Amazon ECS. Há suporte para o Windows, Mac e Linux. Para obter mais informações, consulte AWS Command Line Interface.

- **SDKs da AWS** - fornece APIs específicas de idioma e cuida de muitos dos detalhes da conexão. Elas incluem o cálculo de assinaturas, o tratamento de novas tentativas de solicitação e o tratamento de erros. Para obter mais informações, consulte AWS SDKs.

- **Copilot** - fornece uma ferramenta de código aberto para os desenvolvedores criarem, lançarem, e operarem aplicações em contêineres prontos para produção no Amazon ECS. Para obter mais informações, consulte Copilot no site daGitHub.

- **AWS CDK** - fornece um framework de desenvolvimento de software de código aberto que você pode usar para modelar e provisionar recursos de aplicações em nuvem usando linguagens de programação conhecidas. O AWS CDK provisiona seus recursos de forma segura e repetível por meio do AWS CloudFormation.