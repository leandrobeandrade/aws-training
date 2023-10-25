# ECS - Elastic Container Service

O ECS ajuda você a executar aplicativos em contêineres, sendo um sistema de gestão construído para escala e alto desempenho.

## Contêineres AWS

Os contêineres são populares para implantar e gerenciar aplicativos na nuvem. Os contêineres permitem que você empacote o código em um único objeto, isole o código e remova as dependências de outros componentes. Funciona isoladamente sendo um conceito essencial em arquiteturas de microsserviços. Ter o aplicativo em um contêiner facilita a depuração, isso facilita porque a aplicação fica dentro de um container isolado com o contêiner permanecendo consistente independentemente da implantação.

> Contêineres e Escala

É importante projetar em escala ao usar contêineres, podendo haver dezenas de hosts com centenas de contêineres à medida que o ambiente cresce. Deve-se preparar para saber como gerenciar operações em escala.

## Vantagens

- Execute contêineres na AWS em grande escala sem se preocupar com a infraestrutura subjacente
- Reduza os custos com ajuste de escala automático e preço conforme o uso em várias opções de computação da AWS
- Implemente com mais rapidez e concentre-se em suas aplicações usando o Amazon ECS com a computação com tecnologia sem servidor do AWS Fargate para contêineres
- Crie no Amazon ECS com confiança, sabendo que a segurança, a conformidade e a arquitetura atendem aos padrões regulatórios

## Como funciona

O Amazon Elastic Container Service (Amazon ECS) é um serviço de orquestração de contêineres totalmente gerenciado que simplifica a implantação, o gerenciamento e a escalabilidade de aplicações conteinerizadas. Basta descrever suas aplicação e os recursos necessários, e o Amazon ECS vai executar, monitorar e escalar a aplicação em opções flexíveis de computação com integrações automáticas com outros serviços de suporte da AWS de que sua aplicação precise. Execute operações do sistema, como criar regras personalizadas de escalabilidade e capacidade, além de observar e consultar dados de logs de aplicações e telemetria.

Vem com práticas recomendadas operacionais e de configuração da AWS incorporadas, sendo integrado à AWS e a ferramentas de terceiros, como o Amazon Elastic Container Registry (ECR) e o Docker. Essa integração torna mais fácil para as equipes se concentrarem na criação das aplicações, não no ambiente. Você pode executar e dimensionar suas workloads de contêiner na nuvem e on-premises, sem a complexidade de gerenciar um ambiente de gerenciamento.

## Camadas ECS:

- Capacidade - A infraestrutura em que seus contêineres funcionam
- Controlador - Implante e gerencie seus aplicativos que são executados nos contêineres
- Provisionamento - As ferramentas que você pode usar para interagir com o agendador para implantar e gerenciar seus aplicativos e contêineres

> Capacidade do Amazon ECS

A capacidade do Amazon ECS é a infraestrutura em que seus contêineres são executados. Veja abaixo uma visão geral das opções de capacidade:

- Instâncias do Amazon EC2 na nuvem AWS
- Você escolhe o tipo de instância, o número de instâncias e gerencia a capacidade
- Sem servidor (AWS Fargate) na nuvem AWS        
  - O Fargate é um mecanismo de computação sem servidor pay-as-you-go que lida com o planejamento de capacidade e isola workloads de contêiner para segurança.

- Máquinas virtuais (VM) ou servidores locais
  - O Amazon ECS Anywhere fornece suporte para registrar uma instância externa, como um servidor on-premises ou uma máquina virtual (VM), no cluster do Amazon ECS.

A capacidade pode estar localizada em qualquer um dos seguintes AWS recursos:

- Uma VPC com zonas de disponibilidade
- Local Zones
- Zonas do Wavelength
- Regiões da AWS
- AWS Outposts

> Provisionamento do Amazon ECS

Há várias opções para provisionar o Amazon ECS:

- **AWS Management Console** - fornece uma interface da Web que você pode usar para acessar seus recursos do Amazon ECS.

- **AWS Command Line Interface (AWS CLI)** - fornece comandos para um amplo conjunto de serviços da AWS, incluindo o Amazon ECS. Há suporte para o Windows, Mac e Linux.

- **SDKs da AWS** - fornece APIs específicas de idioma e cuida de muitos dos detalhes da conexão. Elas incluem o cálculo de assinaturas, o tratamento de novas tentativas de solicitação e o tratamento de erros.

- **Copilot** - fornece uma ferramenta de código aberto para os desenvolvedores criarem, lançarem, e operarem aplicações em contêineres prontos para produção no Amazon ECS.

- **AWS CDK** - fornece um framework de desenvolvimento de software de código aberto que você pode usar para modelar e provisionar recursos de aplicações em nuvem usando linguagens de programação conhecidas. O AWS CDK provisiona seus recursos de forma segura e repetível por meio do AWS CloudFormation.
