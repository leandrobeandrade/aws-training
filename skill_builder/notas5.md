# AWS - Anotações gerais

Anotações referentes ao curso [AWS Cloud Practitioner Essentials](https://explore.skillbuilder.aws/learn/course/8287/elementos-essenciais-do-aws-cloud-practitioner-portugues-aws-cloud-practitioner-essentials-portuguese) na plataforma AWS Skill Builder.

## AWS CAF - Cloud Adoption Framework 

Gerencia no processo de migrição para nuvem por meio de orientações, fornecendo aconselhamento à sua empresa para habilitar uma migração rápida e tranquila para a AWS. No nível mais alto do AWS CAF as orientações são organizadas em seis áreas de foco chamadas perspectivas, cada perspectiva aborda responsabilidades distintas. Em geral, as perspectivas de negócio, pessoas e governança se concentram nas capacidades comerciais, enquanto as perspectivas de plataforma, segurança e operações se concentram em capacidades técnicas.

> **perspectiva de negócio**

      Garante que a TI esteja alinhada às necessidades de negócio e que os investimentos em TI estejam vinculados aos 
      principais resultados dos negócios e que suas estratégias e metas de negócios estejam alinhadas com suas estratégias 
      e metas de TI. As funções comuns a perspectiva de negócio são: gerentes de negócios, gerentes financeiros, 
      proprietários de orçamento e stakeholders de estratégia.

> **perspectiva de pessoas**

      Promove o desenvolvimento de uma estratégia de gerenciamento de alterações em toda a organização para a adoção 
      bem-sucedida da nuvem. Avalia estruturas e funções organizacionais, novos requisitos de habilidades e processos e 
      identifica lacunas. Isso ajuda a priorizar treinamento, pessoal e mudanças organizacionais. As funções comuns da 
      perspectiva de pessoas são: recursos humanos, equipe e gerentes de pessoas.

> **perspectiva de governança**

      Concentra-se nas habilidades e nos processos para alinhar as estratégias de TI e de negócios. Isso garante que você 
      maximize o valor comercial e minimize os riscos. Atualiza as habilidades e os processos da equipe necessários para 
      garantir a governança de negócios na nuvem. Gerencia e mensura os investimentos em nuvem para avaliar os resultados de 
      negócios. As funções comuns na perspectiva de governança são: diretor de informações (CIO), gerentes do programa, 
      arquitetos empresariais, analistas de negócios e gerentes de portfólio.

> **perspectiva de plataforma**

      Inclui princípios e padrões para implementação de novas soluções na nuvem e migração de cargas de trabalho locais para 
      a nuvem. Usa uma variedade de modelos arquitetônicos para entender e comunicar a estrutura dos sistemas de TI e suas 
      relações. Descreve a arquitetura do ambiente de destino em detalhes. As funções comuns da perspectiva de plataforma são:
      diretor de tecnologia (CTO), gerentes de TI e arquitetos de soluções.

> **perspectiva de segurança**

      Garante que a organização atenda aos objetivos de segurança de visibilidade, auditoria, controle e agilidade. Estrutura 
      a seleção e a implementação de controles de segurança que atendam às necessidades da organização. As funções comuns da 
      perspectiva de segurança são: diretor de segurança da informação (CISO), gerentes de segurança de TI e analistas de 
      segurança de TI.

> **perspectiva de operações**

      Garante habilitar, executar, usar, operar e recuperar cargas de trabalho de TI para o nível definido com os stakeholders
      da empresa. Define como os negócios diários, trimestrais e anuais são conduzidos. Alinhe e dê suporte às operações do 
      negócio. O AWS CAF ajuda os stakeholders a definir os procedimentos operacionais atuais e identificar mudanças de 
      processo e treinamento necessários para implementar a nuvem com sucesso. As funções comuns da perspectiva de operações 
      são: gerentes de operações de TI e gerentes de suporte de TI.

## Estratégias de migração

Ao migrar aplicativos para a nuvem AWS, seis das estratégias de migração mais comuns que você pode implementar são:

- **Rehosting** - Redefinição de hospedagem

Também conhecida como `lift-and-shift`, envolve a movimentação de aplicativos sem alterações. No cenário de uma grande migração legada, em que a empresa busca implementar sua migração e dimensionar rapidamente para atender a um caso de negócio, a hospedagem da maioria dos aplicativos é redefinida. 

- **Replatforming** - Redefinição de plataforma

Realocação de plataforma, também conhecida como `lift, tinker and shift`, envolve fazer algumas otimizações na nuvem para obter um benefício tangível. A otimização é alcançada sem alterar a arquitetura central do aplicativo.

- **Refactoring** - Refatoração/rearquitetura

Refatoração envolve reimaginar como um aplicativo é arquitetado e desenvolvido usando recursos nativos da nuvem. A refatoração costuma ser orientada pela forte necessidade que a empresa tem de adicionar recursos, scaling ou desempenho que, de outra forma, seriam difíceis de obter no ambiente atual do palicativo.

- **Repurchasing** - Recompra

Recompra envolve a mudança de uma licença tradicional para um modelo de software como serviço. Por exemplo, uma empresa pode optar por implementar a estratégia de recompra migrando de um sistema de gerenciamento de relacionamento com o cliente (CRM) para o Salesforce.com.

- **Retain** - Retenção

Retenção consiste em manter os aplicativos essenciais para a empresa no ambiente de origem. Isso pode incluir aplicativos que exigem refatoração importante antes de serem migrados ou trabalhos que podem ser adiados.

- **Retire** - Inativação/aposentar

Inativação é o processo de remoção de aplicativos que não são mais necessários.

## AWS Snow Family

É uma coleção de dispositivos físicos para transporte físico de até exabytes de dados para dentro e para fora da AWS, consiste nos serviços AWS Snowcone, AWS Snowball e AWS Snowmobile. Esses dispositivos oferecem diferentes pontos de capacidade e a maioria inclui recursos de computação integrados. A AWS é a proprietária e responsável pelo gerenciamento da Snow Family, que integra recursos de segurança, monitoramento, gerenciamento de armazenamento e computação da AWS.

> Snowcone

      É um dispositivo pequeno, robusto e seguro para transferência de dados e computação de borda (EC2 e IoT Greengrass). 
      Ele tem 2 CPUs, 4 GB de memória e 8 TB de armazenamento utilizável. 

> Snowball

      Oferece dois tipos de dispositivos:
      
      - Snowball Edge otimizados para armazenamento que são ideais para migrações de dados 
      de grande escala e fluxos de trabalho de transferência recorrentes, em além da computação local com necessidades 
      maiores de capacidade. Armazenamento: 80 TB de capacidade de disco rígido (HDD) para volumes de blocos e armazenamento 
      de objeto compatível com o Amazon S3, além de unidade de estado sólido (SSD) de 1 TB para volumes de blocos. 
      Computação: 40 vCPUs e 80 GiB de memória para dar suporte a instâncias sbe1 do Amazon EC2 (equivalente a C5).

      - Snowball Edge otimizado para computação fornece recursos de computação poderosos para casos de uso, como machine 
      learning, análise de vídeo em movimento completo, análise e pilhas de computação locais. Armazenamento: capacidade de 
      HDD utilizável de 42 TB para armazenamento de objeto compatível com o Amazon S3 ou volumes de blocos compatíveis com o 
      Amazon EBS e também 7,68 TB de capacidade de SSD NVMe utilizável para volumes de blocos compatíveis com o Amazon EBS. 
      Computação: 52 vCPUs, 208 GiB de memória e uma GPU NVIDIA Tesla V100 opcional. Os dispositivos executam as instâncias 
      sbe-c e sbe-g do Amazon EC2, que são equivalentes às instâncias C5, M5a, G3 e P3.

> Snowmobile

      É um serviço de transferência dados na escala de exabytes usado para mover grandes quantidades de dados para a nuvem. 
      Você pode transferir até 100 petabytes por Snowmobile, um contêiner de transporte reforçado com 13,71 metros de 
      comprimento puxado por um caminhão semirreboque.      

## Inovação

Ao examinar como usar os serviços da AWS, é importante focar nos resultados desejados. Você fica devidamente preparado para impulsionar a inovação na nuvem se conseguir articular claramente as seguintes condições: estado atual, estado desejado, problemas que você está tentando resolver. Considerar alguns dos caminhos que poderá explorar no futuro, enquanto continuar em sua jornada para a nuvem.

### Aplicativos sem servidor

Sem servidor significa que você não precisa administrar, fazer manutenção ou administrar servidores de aplicativos sem o cliente se preocupar com tolerância a falhas ou disponibilidade. O AWS Lambda é um exemplo de um serviço que você pode usar para executar aplicativos sem servidor. Se projetar sua arquitetura para acionar funções do Lambda para executar seu código, você poderá ignorar a necessidade de gerenciar uma frota de servidores. Criar sua arquitetura com aplicativos sem servidor permite que seus desenvolvedores se concentrem no produto principal em vez de gerenciar e operar servidores.

### Inteligência artificial

A AWS oferece uma variedade de serviços com tecnologia de inteligência artificial (IA). Por exemplo, você pode executar as seguintes tarefas: converter fala em texto com o `Amazon Transcribe`, descobrir padrões em texto com o `Amazon Comprehend`, identificar atividades on-line potencialmente fraudulentas com o `Amazon Fraud Detector` e criar chatbots de voz e texto com o `Amazon Lex`.

### Machine Learning

O desenvolvimento tradicional de machine learning (ML) é complexo, caro, demorado e propenso a erros. A AWS oferece o `Amazon SageMaker`, que remove o trabalho difícil do processo e ajuda você a criar, treinar e implantar modelos de ML rapidamente. Você pode usar ML para analisar dados, resolver problemas complexos e prever resultados antes que eles aconteçam.

## AWS Well-Architected Framework

Fornece escopo de como projetar e operar sistemas confiáveis, seguros, eficientes e econômicos na nuvem AWS. Com ele, é possível avaliar de forma consistente suas arquiteturas em relação às melhores práticas e aos princípios de projeto e a identificar áreas para melhorias, se baseia em cinco pilares: 

- Excelência operacional 

      Capacidade de executar e monitorar sistemas para entregar valor comercial e melhorar continuamente os processos e 
      procedimentos de apoio. Os princípios de design para a excelência operacional na nuvem incluem executar operações como 
      código, anotar documentação, antecipar falhas e fazer frequentemente alterações pequenas e reversíveis.

- Segurança

      Inclui a capacidade de proteger informações, sistemas e ativos e, ao mesmo tempo, entregar valor comercial por meio de 
      avaliações de risco e estratégias de mitigação. Ao considerar a segurança de sua arquitetura, aplique estas melhores 
      práticas: automatize as melhores práticas de segurança quando possível, aplique segurança em todas as camadas, 
      proteja os dados em trânsito e em repouso.

- Confiabilidade

      Capacidade de um sistema fazer o seguinte: recuperar-se de interrupções na infraestrutura ou no serviço, Adquirir 
      dinamicamente recursos de computação para atender à demanda, reduzir interrupções, como configurações incorretas ou 
      problemas de rede transitórios, a confiabilidade inclui testes de procedimentos de recuperação, scaling horizontal para
      aumentar a disponibilidade agregada do sistema e recuperação automática de falhas.

- Eficiência de desempenho

      A eficiência de desempenho é a capacidade de usar recursos computacionais com eficiência para cumprir requisitos do 
      sistema e manter essa eficiência à medida que a demanda muda e as tecnologias evoluem. A avaliação da eficiência de 
      desempenho de sua arquitetura inclui experimentar com mais frequência, usar arquiteturas sem servidor e projetar 
      sistemas para ter alcance global em minutos.

- Otimização de custos

      Otimização de custos é a capacidade de executar sistemas para entregar valor comercial com o menor preço. A otimização 
      de custos inclui a adoção de um modelo de consumo, análise e atribuição de despesas e uso de serviços gerenciados para 
      reduzir o custo de propriedade.