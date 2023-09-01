**`01` - Qual serviço AWS ou ferramenta uma empresa deve usar para solicitar e rastrear aumentos de limites do serviço de forma centralizada?**

*R: Service Quotas*
- A empresa deve usar Service Quotas para solicitar e rastrear aumentos de limites dos serviços de forma centralizada. Service Quotas fornece uma visão global dos limites AWS dos serviços usados pela empresa e uma interface centralizada para solicitações de aumento de limites. Além disso, Service Quotas permite que as empresas possam se autogerir e respeitar os limites fixados pelo AWS sem custos adicionais.

**`02` - Uma grande empresa com vários VPCs em várias regiões do mundo precisa conectar e gerenciar centralmente a conectividade de rede entre os seus VPCs. Qual serviço AWS ou recurso atende a esses requisitos?**

*R: AWS Transit Gateway*
- A AWS Transit Gateway é a solução para conectar e centralmente gerenciar a conectividade de rede entre VPCs em várias regiões. Uma Transit Gateway é um serviço que conecta todos os seus recursos da AWS à nível de rede em uma única interface, centralizando a conectividade de rede entre suas VPCs, redirecionadores da AWS e outros recursos na AWS. Ela simplifica e automatiza a implantação de conexões entre suas redes da AWS e ativa e monitora essas conexões. Ela também oferece uma camada de segurança adicional, permitindo que você implante políticas de acesso à nível de rede consistentes entre todos os seus recursos da AWS.

**`03` - Qual serviço ou recurso da AWS verifica as políticas de acesso e oferece recomendações práticas para ajudar os usuários a configurar políticas seguras e funcionais?**

*R: AWS IAM Access Analyzer*
- A AWS IAM Access Analyzer monitora contas, grupos e políticas AWS Identity and Access Management (IAM) para identificar seções de recursos na AWS com configurações de acesso abertas. A ferramenta oferece recomendações práticas que ajudam os usuários a estabelecer políticas de acesso seguras e funcionais.

**`04` - Uma empresa está planejando executar um aplicativo de marketing global na AWS Cloud. O aplicativo terá vídeos que podem ser visualizados pelos usuários. A empresa deve garantir que todos os usuários possam visualizar esses vídeos com baixa latência. Qual serviço da AWS a empresa deve usar para atender a esse requisito?**

*R: AWS CloudFront*
- A empresa deve usar o serviço Amazon CloudFront para atender aos requisitos de visualização de vídeos com baixa latência. O CloudFront é uma rede de entrega de conteúdo (CDN) que ajuda a melhorar a velocidade de entrega de conteúdo, incluindo vídeos, aos usuários finais em todo o mundo. Isso garante uma experiência de visualização suave e sem interrupções para os usuários, independentemente da sua localização geográfica.

**`05` - Uma empresa de mídia global usa a AWS Organizations para gerenciar várias contas da AWS. Que serviço ou recurso da AWS a empresa pode usar para limitar o acesso a serviços da AWS para contas membro?**

*R: Políticas de controle de serviço (SCPs)*
- A opção "Políticas de controle de serviço (SCPs)" está correta porque as Service Control Policies (SCPs) são especificamente projetadas para limitar o acesso aos serviços da AWS para contas de membro dentro de uma organização gerenciada pelo AWS Organizations.

**`06` - Uma empresa deseja implementar a detecção de ameaças em sua infraestrutura AWS. No entanto, a empresa não deseja implantar software adicional. Qual serviço da AWS a empresa deve usar para atender a esses requisitos?**

*R: AWS GuardDuty*
- A empresa deve usar o serviço Amazon GuardDuty para atender aos seus requisitos de detecção de ameaças. GuardDuty é um serviço de monitoramento de segurança que proporciona detecção de ameaças avançada através de deep learning sobre fluxos de dados em reflexo no log de segurança AWS (VPC Flow Logs e CloudTrail). Este serviço é entregue em tempo real e é executado em infraestruturas em nuvem para oferecer atualizações contínuas.

**`07` - Quais das seguintes opções estão incluídas na AWS Enterprise Support? (Escolha duas)**

*R: Suporte à integração de software de terceiros à AWS, Gerente de conta técnica(TAM)*
- O Gerente de Conta Técnica (TAM) AWS oferece consultoria especializada e suporte técnico para empresas que usam os serviços AWS. Os serviços profissionais da AWS fornecem serviços de consultoria de alto nível, treinamento, planejamento, arquitetura e migração. Suporte à integração de software de terceiros à AWS é parte do serviço Enterprise Support AWS. A enterprise support não oferece um tempo de resposta de 5 minutos para problemas críticos.

**`08` - Qual tarefa requer o uso de credenciais de usuário root da conta AWS?**

*R: Mudar plano de suporte AWS*
- A alteração do plano de suporte da AWS requer o uso de credenciais de usuário root da conta da AWS, pois exige uma ação que impacta em toda a conta ou recursos. O acesso de usuário raiz tem privilégios para executar ações que nem todos os usuários da conta devem realizar.

**`09` - Que serviço AWS usa localidades de borda (edge locations)?**

*R: AWS Global Accelerator*
- O AWS Global Accelerator usa localidades de borda em todo o mundo, fornecendo caminhos de baixa latência entre os usuários finais e os seus aplicativos na AWS. O Global Accelerator está na mesma categoria de serviços que a Rede de entrega de conteúdo (CDN) daAmazon aws chamada CloudFront e não está relacionada com as soluções de dados como o Amazon Aurora.

**`10` - Uma empresa deseja migrar uma aplicação crítica para a AWS. A aplicação tem um tempo de execução curto. A aplicação é invocada por mudanças nos dados ou por deslocamentos no estado do sistema. A empresa precisa de uma solução de computação que maximize a eficiência operacional e minimize o custo de execução da aplicação. Qual a solução AWS que a empresa deve usar para cumprir esses requisitos?**

*R: AWS EC2 Spot Instâncias*
- A AWS Lambda é uma solução ideal para a empresa para que ela possa minimizar seus custos de execução da aplicação. A Lambda é um serviço de computação sem servidor que gerencia o código da aplicação e seu ambiente de execução. A Lambda pode ser acionada com base em alterações de dados ou eventos de sistema e a empresa paga apenas o tempo de execução real usado, ajudando a minimizar os custos operacionais.

**`11` - Qual são as responsabilidades de uma empresa que está usando a AWS Lambda? (Escolha dois)**

*R: Escrevendo a atualizando código, Segrunça dentro do código*
- Uma empresa que está usando a AWS Lambda deve ser responsável pela segurança dentro do próprio código e escrever e atualizar o código. A AWS Lambda também oferece serviços para segurança da infra-estrutura subjacente, mas a seleção de recursos de CPU e a empacotagem do sistema operacional não são responsabilidades dessa companhia.

**`12` - Uma empresa quer usar a nuvem AWS para prover acesso seguro a aplicativos desktop que estão sendo executados em um ambiente totalmente gerenciado. Qual serviço AWS deve a empresa usar para atender ao requisito?**

*R: AWS AppSync*
- Amazon AppStream 2.0 é um serviço fornecido pela AWS que permite transmitir aplicativos de desktop de forma segura a partir da nuvem para dispositivos dos usuários. Ele fornece um ambiente totalmente gerenciado para executar e transmitir aplicativos de desktop, garantindo que os aplicativos não sejam instalados ou executados localmente nos dispositivos dos usuários.

**`13` - Quais das seguintes são características das ACLs de rede, conforme usadas na AWS Cloud? (Escolha duas)**

*R: Serviços stateless, operam no vível da instância*
- Eles não têm estado: Network ACLs na AWS não têm estado, o que significa que não acompanham o estado de uma conexão. Cada regra Network ACL é avaliada de forma independente e não está ciente dos pacotes anteriores ou subsequentes na mesma conexão. Eles processam as regras em ordem, começando com a regra de número mais baixo, ao decidir se permitem o tráfego: Network ACLs avaliam as regras em ordem sequencial, começando com a regra de número mais baixo. Depois que uma regra corresponde a um pacote, a decisão de permitir ou negar o tráfego é tomada e a avaliação adicional das regras é interrompida. Esse processamento sequencial de regras é uma característica importante das Network ACLs na AWS.

**`14` - Uma empresa deseja lançar sua carga de trabalho na AWS e precisa que o sistema se recupere automaticamente de falhas. Qual pilares do AWS Well-Architected Framework inclui este requisito?**

*R: Confiabilidade*
- A Confiabilidade é um dos pilares do AWS Well-Architected Framework que inclui esse requisito. A Confiabilidade lida com como você projeta a fiabilidade e a disponibilidade do sistema e como ele pode monitorar as falhas e recuperar após falhas, garantindo que o atendimento aos objetivos de serviço seja atendido.

**`15` - Um usuário precisa determinar se os grupos de segurança de uma instância Amazon EC2 foram modificados no último mês. Como o usuário pode ver se uma alteração foi feita?**

*R: Usar o AWS CloudTrail para ver se o grupo de segurança foi alterado*
- O usuário deve usar o serviço AWS CloudTrail para ver se alguma alteração foi feita no grupo de segurança. O CloudTrail monitora suas API na AWS e fornece logs de auditores que registram qualquer API chamada feita pelo seu usuário, por um serviço da AWS ou por terceiros. Dessa forma, o usuário pode verificar quando houve alterações, com quem foi feita a alteração e qual foi a alteração realizada.

**`16` - Uma empresa está desenvolvendo um aplicativo móvel que precisa de um banco de dados NoSQL de alta performance. Quais serviços AWS a empresa poderia usar para esse banco de dados? (Escolha dois.)**

*R: AWS DynamoDB, AWS DocumentDB (com compatibilidade MongoDB)*
- Ambos os serviços são projetados para oferecer escalabilidade e desempenho para aplicativos modernos. Amazon DynamoDB: É um serviço de banco de dados NoSQL totalmente gerenciado que oferece alta disponibilidade, escalabilidade automática e baixa latência. Ele é adequado para aplicativos com carga de trabalho variável e exigências de desempenho que podem mudar com o tempo. Amazon DocumentDB (com compatibilidade MongoDB): É um serviço de banco de dados gerenciado compatível com MongoDB, que oferece escalabilidade, alta disponibilidade e desempenho para cargas de trabalho de aplicativos que dependem do modelo de documento. Ambos os serviços oferecem características específicas que podem atender às necessidades de desempenho e escalabilidade do aplicativo móvel em desenvolvimento. A escolha entre eles dependerá das necessidades específicas do aplicativo e das preferências da equipe de desenvolvimento.

**`17` - Um usuário deseja implantar um serviço na AWS Cloud, usando princípios de infraestrutura como código (IaC). Qual serviço AWS pode ser usado para atender a esse requisito?**

*R: AWS CloudFormation*
- O AWS CloudFormation fornece modelos de serviços de infraestrutura como código (IaC) que permitem que você crie e gerencie facilmente serviços de nuvem da AWS, além de que seus grupos e suas equipes possam criar infraestruturas da AWS rapidamente, automaticamente, em configurações consistentes e altamente disponíveis. Ele fornece modelos reutilizáveis chamados modelos AWS CloudFormation, que permitem criar e gerenciar facilmente infraestruturas como código.

**`18` - Qual é o escopo de uma VPC na rede AWS?**

*R: A VPC deve abranger pelo menos duas sub-redes em cada Região AWS*
- O escopo de uma VPC é limitado a uma Região AWS e, dentro desse escopo, uma VPC pode se estender para uma ou mais Zonas de Disponibilidade.

**`19` - Uma empresa que possui várias unidades de negócio deseja gerenciar e governar centralmente os seus ambientes da AWS Cloud. A empresa deseja automatizar a criação de contas da AWS, aplicar políticas de controle de serviços (SCPs) e simplificar processos de faturamento. Qual serviço ou ferramenta da AWS a empresa deve usar para atender a essas exigências?**

*R: AWS Organizations*
- A empresa deve usar o AWS Organizations para atender a essas exigências. O AWS Organizations torna mais fácil para você criar e gerenciar contas da AWS e aplicar políticas de controle de serviços uniformemente a todas as suas contas da AWS. O AWS Organizations também ajuda na simplificação dos processos de faturamento com recibos unificados e pagamentos consolidados.

**`20` - Qual serviço AWS pode ajudar a proteger aplicativos que executam na AWS de ataques DDoS?**

*R: AWS Shield*
- O AWS Shield é um conjunto de serviços de proteção DDoS, que ajuda a proteger as aplicações que rodam na AWS Cloud contra os ataques que ocorrem na rede. Estes serviços são baseados em DDoS proteção padrão e DDoS proteção avançada que oferecem detectar, mitigar e defense contra DDoS attacks.

**`21` - Uma empresa online estava executando uma carga de trabalho on premise e estava tendo problemas para lançar novos produtos e recursos. Após migrar a carga de trabalho para a AWS, a empresa pode lançar rapidamente produtos e recursos e pode dimensionar sua infraestrutura conforme necessário. Qual da seguinte proposição de valor da AWS esse cenário descreve?**

*R: Agilidade de negócios*
- Este cenário descreve o conceito de agilidade de negócios, em que as organizações precisam de velocidade para responder às demandas de mercado e poder dar a partida em novos produtos e recursos o mais rápido possível. A AWS oferece um ambiente dinâmico que facilita a rápida implementação, teste e lançamento de produtos e recursos rapidamente.

**`22` - Uma empresa planeja migrar sistemas legados complexos para a AWS. A empresa usará vários sistemas operacionais, vários bancos de dados e várias linguagens de programação. Qual o benefício da Nuvem AWS que esse cenário representa?**

*R: Segurança*
- O cenário descrito apresenta benefícios de segurança para a Nuvem AWS. A AWS disponibiliza recursos e serviços integralmente projetados para oferecer segurança em todas as camadas da infraestrutura. A AWS é totalmente certificada sob as auditações mais exigentes. Isso oferece proteção sólida e confiável para os sistemas críticos e legados e garante a manutenção da segurança e da conformidade mesmo durante mudanças significativas nas soluções de infraestrutura.

**`23` - Como o modelo de preços da AWS Cloud difere do modelo tradicional de custos de armazenamento de on-premises?**

*R: Não há compromissos de custos adiantados*
- A opção "Não há compromissos de custos adiantados" está correta porque o modelo de definição de preço da nuvem da AWS difere do modelo tradicional de definição de preço de armazenamento on premise, eliminando compromissos de custo inicial. Em um modelo tradicional de armazenamento on premise, as organizações geralmente precisam investir uma quantia significativa de capital antecipadamente para comprar hardware, licenças de software e equipamentos de infraestrutura. Esses custos iniciais podem ser substanciais e geralmente exigem compromissos de longo prazo.

**`24` - Uma empresa deseja melhorar a disponibilidade geral e o desempenho dos seus aplicativos hospedados na AWS. Qual serviço da AWS a empresa deve usar?**

*R: AWS Lightsail*
- A empresa deve usar o serviço AWS Global Accelerator para melhorar a disponibilidade e o desempenho das suas aplicações hospedadas na AWS. O Global Accelerator fornece aos usuários finais de alto desempenho e baixa latência, fornecendo acesso a zonas de disponibilidade da AWS. A tecnologia Smart Routing do Global Accelerator identifica automaticamente os usuários finais mais próximos e direciona o tráfego deles para os melhores endpoints de endpoint.

**`25` - A AWS tem a capacidade de alcançar preços pay-as-you-go (pré-pago) mais baixos, agregando o uso de centenas de milhares de usuários. Isso descreve qual vantagem da AWS Cloud?**

*R: Alta economia de escala*
- A AWS Cloud oferece vantagens como altas economias de escala, consequentes de seus modelos de pagamento por uso, alcançando preços mais baixos ao agregar o uso de centenas de milhares de usuários.

**`26` - Qual documentação o AWS Artifact fornece?**

*R: Certificações ISO do AWS*
- O AWS Artifact fornece documentação relacionada à certificações de conformidade, incluindo certificações ISO. O AWS Artifact é um dispositivo online que permite a você obter documentos de conformidade da AWS, como certificações ISO de conformidade, documentos de potencial de assumir responsabilidade, conformidades ATO e certificações PCI DSS.

**`27` - Uma empresa precisa maximizar sua capacidade de se adaptar às mudanças nas necessidades dos negócios, sem comprometer seu orçamento. Qual estratégia a empresa deve implementar para atender a esses requisitos?**

*R: Usar Saving Plans*
- A empresa deve usar preços pagos à medida que você vai usando. A cobrança à medida que você vai usando fornece economias significativas de custos ao se adaptar às mudanças na demanda, permitindo que a empresa evite prescrições de custos desnecessários e overprovisioning.

**`28` - Uma empresa possui um servidor de banco de dados que está sempre executando. A empresa hospeda o banco de dados em instâncias Amazon EC2. O tamanho das instâncias é adequado para a carga de trabalho. A carga de trabalho vai rodar por 1 ano. Qual opção de compra de instância EC2 satisfará esses requisitos de maneira MAIS eficaz em custos?**

*R: Standard Reserved Instances*
- As Instâncias Reservadas Padrão são as opções de compra de instâncias EC2 mais rentáveis para a carga de trabalho aqui descrita. Neste planejamento, é possível pagar um preço mais baixo e obter um desconto significativo em relação às instâncias On-Demand, garantindo preços previsíveis. Além disso, o custo total envolvido no uso de instâncias reservadas será menor do que o das instâncias Spot.

**`29` - Uma empresa deseja revisar seus custos mensais de uso do Amazon EC2 e do Amazon RDS nos últimos anos. Qual serviço AWS ou ferramenta fornece essas informações?**

*R: Cost Explorer*
- A Cost Explorer ajuda as empresas a obter uma visão transparente dos custos de uso da Amazon Web Services (AWS). A ferramenta permite a visualização de custos históricos e a previsão futura a partir de dashboards, relatórios em gráficos, downloads e muito mais.

**`30` - Qual serviço AWS pode ser usado para criptografar dados?**

*R: AWS KMS (Key Management Service)*
- O AWS Key Management Service (KMS) pode ser usado para criptografar os dados de repouso na AWS. Ele cria e gerencia as chaves de criptografia para proteger os dados, em que as chaves não ficam nos discos e é possível fazer a recuperação delas em casos de perda. O KMS garante que todas as chaves e o conteúdo sejam protegidos com certificados SSL/TLS. Referência: https://aws.amazon.com/blogs/security/how-to-protect-data-at-rest-with-amazon-ec2-instance-store-encryption/

**`31` - Uma empresa deseja migrar seus aplicativos de seu data center local para um VPC na AWS Cloud. Esses aplicativos precisarão acessar recursos localmente. Quais ações atenderão a esses requisitos? (Escolha duas.)**

*R: Criar uma conexão VPN entre um dispositivo local e um Gateway privado virtual no VPC, configurar uma conexão AWS Direct Coonect entre o data center local e a AWS*
- Crie uma conexão VPN entre um dispositivo local e um gateway privado virtual na VPC: Ao configurar uma conexão VPN (Virtual Private Network) entre um dispositivo local (como um roteador) e um gateway privado virtual na VPC, a empresa pode estabelecer uma conexão segura e criptografada entre sua rede local e a VPC na AWS. Isso permite que os aplicativos em execução na VPC acessem com segurança os recursos locais por meio da conexão VPN. Configure uma conexão AWS Direct Connect entre o datacenter local e a AWS: O AWS Direct Connect fornece uma conexão de rede dedicada entre o data center local da empresa e a AWS. Ao configurar essa conexão, a empresa pode estabelecer um link de alta velocidade e baixa latência diretamente para a AWS, ignorando a Internet pública. Isso permite que os aplicativos executados na VPC tenham acesso rápido e confiável aos recursos locais.

**`32` - Uma empresa deseja executar cargas de trabalho de produção na AWS. A empresa precisa de um serviço de concierge, um gerente de conta técnica AWS designado (TAM) e suporte técnico que esteja disponível 24 horas por dia, 7 dias por semana. Que plano de suporte AWS atenderá a esses requisitos?**

*R: AWS Enterprise Support*
- O plano de suporte AWS Enterprise será o único que atenderá aos requisitos, pois inclui um gerente de conta técnica designado, chamado TAM, e suporte técnico 24 horas por dia, 7 dias por semana.

**`33` - Uma empresa precisa processar centenas de solicitações simultaneamente de diferentes usuários. Qual é a combinação de serviços AWS que a empresa deve usar para construir uma solução operacionalmente eficiente?**

*R: AWS SQS (Simple Queue Service) e AWS Lambda*
- A opção "AWS SQS e AWS Lambda" é correta porque combina dois serviços da AWS, Amazon Simple Queue Service (Amazon SQS) e AWS Lambda, para criar uma solução operacionalmente eficiente para processar várias solicitações de diferentes usuários. O Amazon SQS é um serviço de enfileiramento de mensagens totalmente gerenciado que permite desacoplar os componentes em um aplicativo, permitindo a comunicação assíncrona entre eles. Ele fornece uma maneira confiável e escalável de lidar com mensagens e atua como um buffer entre os componentes, garantindo que as mensagens sejam processadas com eficiência. Nesse caso, a empresa pode usar o Amazon SQS para receber e armazenar as solicitações recebidas de diferentes usuários.

**`34` - Uma empresa precisa visualizar graficamente cobrança e uso da AWS ao longo do tempo. A empresa também precisa de informações sobre seus custos mensais da AWS. Qual ferramenta de Gerenciamento de Cobrança e Custos da AWS oferece esses dados em formato gráfico?**

*R: Cost Emplorer*
- A pesquisa "Cost Explorer" da AWS permite que as organizações visualize gráficos de seus custos e uso da AWS. O Cost Explorer permite que você analise os custos mensais, trimestrais, semestrais ou anuais da AWS em visualizações gráficas e facilite a compreensão e otimização dos custos da AWS.

**`35` - Qual princípio de design de arquitetura descreve a necessidade de isolar falhas entre componentes dependentes na AWS Cloud?**

*R: Fraco acoplamento*
- O princípio de design arquitetônico de isolar falhas entre componentes dependentes tem por objetivo minimizar a complexidade de operações entre componentes. Isso é conhecido como principio de acoplação fraca, que busca garantir que mudanças em um componente não afetem outros componentes e que a falha em um dos componentes não tenha um impacto massivo nas outras.

**`36` - Uma empresa está lançando um aplicativo de comércio eletrônico que deve estar sempre disponível. O aplicativo será executado em instâncias Amazon EC2 continuamente nos próximos 12 meses. Qual é a opção de compra de instância MAIS econômica que atenda a esses requisitos?**

*R: Savings Plans*
- Saving Plans são a opção mais econômica para atender aos requisitos da empresa pois oferecem um desconto previsível sobre os custos das instâncias de forma a longo prazo.

**`37` - Qual serviço ou recurso AWS atua como um firewall para instâncias do Amazon EC2?**

*R: Security group (Grupo de segurança)*
- Um grupo de segurança consiste em uma coleção de regras de segurança que controlam o tráfego de entrada e saída para um ou mais enlaces de recursos AWS. Os Security Groups podem ser usados como firewalls para Amazon EC2 instâncias, filtrando o tráfego conforme solicitado pelas regras definidas.

**`38` - Qual serviço da AWS usa aprendizado de máquina para ajudar a descobrir, monitorar e proteger dados sensíveis armazenados em buckets Amazon S3?**

*R: AWS Macie*
- A Amazon Macie usa aprendizado de máquina para monitorar e classificar acessos não autorizados ou suspeitos a dados armazenados nos buckets Amazon S3, melhorando assim a proteção de informações confidenciais. Macie identifica automaticamente os dados confidenciais, monitora o risco da exposição e fornece medidas de conformidade.

**`39` - Um novo usuário da AWS que tem pouca experiência na nuvem deseja construir um aplicativo usando serviços AWS. O usuário deseja aprender como implementar serviços específicos AWS pelos exemplos de outros clientes. O usuário também deseja fazer perguntas a especialistas AWS. Qual serviço ou recurso AWS atenderá a esses requisitos?**

*R: AWS Health Dashboard*
- O AWS Health Dashboard é um recurso para acompanhar as notificações de saúde da AWS. Possui recursos intuitivos para ajudar os usuários a entender e lidar com a saúde das serviços AWS. Esses recursos incluem executar pesquisas sobre incidentes passados, acompanhar incidentes atuais e receber alertas de novos incidentes. Além disso, um usuário pode ver os detalhes dos incidentes, examinar a tecnologia básica por trás do serviço afetado e navegar na lista de serviços ou empresas afetadas.

**`40` - O usuário está comparando as opções de compra para uma aplicação que roda no Amazon EC2 e Amazon RDS. A aplicação não pode suportar nenhuma interrupção. A aplicação experimenta uma quantidade previsível de uso, incluindo alguns picos sazonais que duram apenas algumas semanas de cada vez. Não é possível modificar a aplicação. Qual opção de compra atende a esses requisitos da MANEIRA MAIS custo-efetiva?**

*R: Compre instâncias reservadas para a quantidade prevista de uso ao longo do ano. Permita que qualquer uso sazonal seja executado em uma taxa sob demanda*
- Comprar instâncias reservadas para a quantidade prevista de uso ao longo do ano: Isso garante que a carga de uso previsível esteja coberta por instâncias reservadas, que geralmente são mais econômicas em comparação com as instâncias sob demanda. Dessa forma, você estará economizando custos na execução contínua da aplicação. Permitir que qualquer uso sazonal seja executado em instâncias Spot: As instâncias Spot são conhecidas por serem muito mais baratas, mas sua disponibilidade não é garantida, e o preço pode variar de acordo com a demanda do mercado. Como a aplicação experimenta picos sazonais que duram apenas algumas semanas de cada vez, você pode se beneficiar dos preços baixos das instâncias Spot durante esses períodos. Ao escolher essa opção, você estará aproveitando o melhor dos dois mundos: a previsibilidade e economia das instâncias reservadas para a carga principal e a economia adicional das instâncias Spot para os períodos de pico sazonal. Isso torna essa opção a mais adequada em termos de custo-efetividade, considerando os requisitos da aplicação.

**`41` - Uma empresa tinha um ciclo de implantação de aplicativos On-Premises de 3 a 4 semanas. Após a migração para a AWS Cloud, a empresa consegue implantar o aplicativo em 2 a 3 dias. Qual benefício essa empresa experimentou ao se mudar para a AWS Cloud?**

*R: Agilidade*
- Agilidade refere-se à capacidade de se adaptar rápida e facilmente a circunstâncias, demandas ou requisitos em constante mudança. No cenário em questão, a empresa experimentou uma melhoria significativa em seu ciclo de implantação de aplicativos após a migração para a Nuvem AWS. O tempo de implantação foi reduzido de 3 a 4 semanas no ambiente local para 2 a 3 dias na Nuvem AWS.

**`42` - Quais são algumas vantagens de usar instâncias Amazon EC2 para hospedar aplicativos na AWS Cloud em vez de on premise? (Escolha dois)**

*R: Integração do EC2 com o AWS VPC, o AWS cloudTrrail e o AWS IAM, modelo de preços flexíveis de pagamento conforme a utilização do EC2*
- O EC2 integra-se com Amazon VPC, AWS CloudTrail e AWS Identity and Access Management (IAM): as instâncias do EC2 podem ser facilmente integradas a outros serviços da AWS, como Amazon VPC para rede, AWS CloudTrail para auditoria e monitoramento e AWS IAM para gerenciamento acesso e permissões. Essa integração fornece uma infraestrutura perfeita e abrangente para hospedar aplicativos na Nuvem AWS. O EC2 tem um modelo de precificação flexível de pagamento conforme o uso: Com o EC2, você pode escolher entre várias opções de precificação, incluindo instâncias sob demanda, instâncias reservadas e instâncias spot. Essa flexibilidade permite que você otimize os custos com base nos requisitos e padrões de uso de seu aplicativo. Você paga apenas pelos recursos de computação que realmente consome, o que pode ser mais econômico em comparação com a configuração e manutenção da infraestrutura local, na qual você precisa estimar e provisionar recursos com antecedência.

**`43` - Qual serviço AWS ou recurso identifica se um bucket da Amazon S3 ou uma função IAM foi compartilhada com uma entidade externa?**

*R: AWS IAM Access Analyzer*
- O AWS IAM Access Analyzer ajuda o usuário a identificar se há compartilhamentos inadequados de recursos do AWS, como contas, funções da IAM e buckets da Amazon S3. O Access Analyzer vê recursos compartilhados entre contas da AWS e entidades externas, com ou sem direitos, sejam elas entidades governamentais, outras empresas e bancos de dados.

**`44` - Uma empresa planeja criar um data lake que utilize o Amazon S3. Qual opção terá o MAIOR efeito no custo?**

*R: Escolha de camadas de armazenamento S3*
- A escolha das camadas de armazenamento S3 terá o maior efeito no custo do projeto de data lake. O S3 oferece 3 camadas de armazenamento: padrão, Infrequente (IA) e Acesso de Gravação Rápida (RRS). Novos objetos armazenados inicialmente em S3 Standard são armazenados em camadas IA ou RRS com base na frequência com a qual eles são acessados. Isso significa que a camada de armazenamento que escolher pode ter grande impacto no custo total do projeto.

**`45` - Uma empresa projetou sua infraestrutura da AWS Cloud para executar suas cargas de trabalho de maneira eficaz. A empresa também tem protocolos para melhorar continuamente os processos de suporte. Qual pilastra da AWS Well-Architected Framework esse cenário representa?**

*R: Excelência operacional*
- Esta cenário representa a pilastra da Excelência Operacional. De acordo com o AWS Framework Well-Architected, a Excelência Operacional é o relatório com o processo de gerenciamento operacional de sistemas para obter eficiência de serviço. Isso envolve iniciativas para executar as operações da forma mais eficiente possível, incluindo a melhoria contínua dos processos em execução hospedados na nuvem.

**`46` - Uma grande empresa possui vários departamentos, cada um com uma conta aws. Cada departamento já comprou instâncias reservadas do Amazon EC2. Alguns departamentos não usam todas as instâncias reservadas que compraram e outros precisam de mais instâncias reservadas do que compraram. A empresa precisa gerenciar as contas da AWS para todos os departamento para que eles possam compartilhar as instâncias reservadas. Qual serviço ou ferramenta da AWS a empresa deve usar para atender a esses requisitos?**

*R: AWS Organizations*
- O AWS Organizations é um serviço fornecido pela Amazon Web Services que permite à empresa gerenciar centralmente várias contas da AWS. Ele permite que a empresa organize essas contas de forma hierárquica, com uma conta máster e contas subordinadas para cada departamento.

**`47` - Qual dos seguintes são componentes de uma conexão de VPN Site-to-Site da AWS? (Escolha dois.)**

*R: Customer gateway, Virtual private gateway*
- Os componentes de uma conexão de VPN Site-to-Site da AWS são o Customer Gateway (CGw) e o Virtual Private Gateway (VGW). O CGw é um dispositivo que conecta sua rede local à rede da VPC, onde sua VGW é implantada. A VGW atuará como sua "porta de saída" para a sua VPC durante a conexão VPN Site-to-Site.

**`48` - Qual serviço AWS deve ser usado para monitorar as instâncias Amazon EC2 para utilização de CPU e rede?**

*R: AWS CloudWatch*
- A Amazon CloudWatch deve ser usada para monitorar as instâncias Amazon EC2 para utilização de CPU e rede. O CloudWatch usa log metrics e alarme para monitorar os recursos de infraestrutura e aplicações e pode identificar tendências e pontos de dados para ajudar a otimizar o desempenho. Além disso, é possível definir alarme que são acionados quando os limites de uso definidos são atingidos.

**`49` - Uma empresa possui uma frota de navios de carga. Os navios de carga possuem sensores que coletam dados no mar, onde há conectividade à internet intermitente ou nenhuma conectividade. A empresa precisa coletar, formatar e processar os dados no mar e mover os dados para a AWS posteriormente. Qual serviço AWS a empresa deve usar para atender a esses requisitos?**

*R: AWS Snowball Edge*
- O AWS Snowball Edge é um serviço que combina capacidades de armazenamento e computação em um dispositivo portátil. Ele foi projetado para situações em que há conectividade limitada ou inexistente com a internet, tornando-o ideal para coletar, formatar e processar dados em alto mar. Os dispositivos Snowball Edge são robustos e podem ser implantados em locais remotos, incluindo em navios de carga.

**`50` - Uma empresa deseja limitar o acesso ao seu conjunto de empregados para um portifólio de recursos AWS pré-definidos. Qual solução AWS a empresa deve usar para atender a esse requisito?**

*R: AWS Service Catalog*
- Para limitar o acesso ao conjunto de empregados para um portfólio de recursos AWS pré-definidos, a solução mais adequada a ser utilizada é o AWS Service Catalog. O AWS Service Catalog permite que as empresas criem e gerenciem um catálogo de serviços e recursos pré-aprovados que os usuários podem provisionar e implantar de maneira autosserviço. Com o AWS Service Catalog, a empresa pode controlar quais serviços e recursos específicos estão disponíveis para os seus empregados, limitando suas opções a um conjunto pré-definido de escolhas. O AWS Config é uma ferramenta para avaliar e auditar as configurações dos recursos da AWS, não sendo a melhor opção para limitar o acesso a recursos específicos. Os AWS SDKs (Software Development Kits) são conjuntos de bibliotecas de programação que permitem que os desenvolvedores interajam com os serviços da AWS em suas aplicações. Eles não têm como objetivo limitar o acesso a recursos específicos para um conjunto de empregados. O AWS AppSync é um serviço de back-end totalmente gerenciado que facilita o desenvolvimento de aplicativos móveis e web escaláveis, mas também não se enquadra na categoria de solução para limitar o acesso a recursos específicos. Portanto, a resposta correta para atender ao requisito de limitar o acesso a um portfólio de recursos AWS pré-definidos é o AWS Service Catalog.

**`51` - Uma empresa precisa instalar uma aplicação em um container Docker. Qual serviço AWS elimina a necessidade de provisionar e gerenciar os hosts de container?**

*R: AWS Fargate*
- O AWS Fargate é um mecanismo de computação para Amazon Elastic Container Service (ECS) e Amazon Elastic Kubernetes Service (EKS) que permite executar contêineres sem a necessidade de gerenciar a infraestrutura subjacente. Com o AWS Fargate, você não precisa provisionar ou gerenciar os hosts de contêiner diretamente. Em vez disso, você pode se concentrar em definir e executar seus aplicativos em contêineres, e o AWS Fargate se encarrega de iniciar os contêineres e dimensionar a infraestrutura com base nas necessidades de seu aplicativo.

**`52` - Uma empresa está planejando substituir seus servidores de computação físicos próprios pelos serviços de computação sem servidor da AWS. A empresa deseja poder aproveitar rapidamente as tecnologias avançadas após a migração. Qual dos pilares do AWS Well-Architected Framework representa esse plano?**

*R: Eficiência de desempenho*
- Esse plano representa o pilar de Eficiência de Desempenho do AWS Well-Architected Framework. Espera-se que a empresa tenha o objetivo de aproveitar as melhorias no tempo de resposta da aplicação, custo de gerenciamento e diminuição de complexidade de implantação e manutenção, que os serviços sem servidor podem fornecer após a migração.

**`53` - Qual serviço AWS suporta a criação de relatórios visuais a partir dos dados do relatório de custo e uso da AWS?**

*R: AWS QuickSight*
- O Amazon QuickSight é um serviço de business intelligence (BI) fornecido pela AWS que permite criar relatórios visuais, painéis e visualizações interativas de dados. Ele oferece suporte à criação de relatórios visuais de várias fontes de dados, incluindo dados do AWS Cost and Usage Report. Com o Amazon QuickSight, você pode se conectar aos dados do Relatório de custos e uso da AWS e criar facilmente visualizações para obter insights sobre seus gastos e uso da AWS. Você pode criar tabelas, gráficos e tabelas para analisar seus custos, identificar tendências e rastrear seus padrões de uso. O QuickSight fornece uma interface amigável e oferece várias opções de visualização e recursos de personalização para criar relatórios visualmente atraentes e informativos.

**`54` - Qual característica da nuvem AWS ajuda os usuários a eliminar capacidade de CPU não utilizada?**

*R: Elasticidade*
- A elasticidade da nuvem AWS ajuda os usuários a eliminar o desperdício de capacidade de CPU, ao dimensionar as suas instâncias de acordo com a necessidade. Por exemplo, os usuários podem aumentar ou diminuir a capacidade da CPU somente quando necessário, ou aumentar efetivamente a capacidade de processamento em incrementos pequenos. A elasticidade fornece aos usuários a capacidade de dimensionar o seu ambiente rapidamente, ao mesmo tempo em que reduz os custos.

**`55` - Uma empresa está lançando um aplicativo na AWS Cloud. O aplicativo usará o armazenamento Amazon S3. Uma grande equipe de pesquisadores terá acesso compartilhado aos dados. A empresa deve ser capaz de recuperar dados que são sobrescritos ou excluídos acidentalmente. Qual recurso do S3 a empresa deve ativar para atender a esse requisito?**

*R: Versão S3*
- A empresa deve habilitar a versão S3. O S3 de versionamento fornece segurança e recuperação aprimoradas para os objetos em seus buckets S3, permitindo que você recupere facilmente objetos excluídos ou sobrescritos. Isso permite que os usuários trabalhem com mais confiança, ao prover a capacidade de rastrear, recuperar e rever uma versão específica de um arquivo.

**`56` - Uma empresa deseja migrar seus workloads para a AWS, mas ela não possui especialização em computação na nuvem AWS. Qual serviço ou recurso AWS ajudará a empresa com sua migração?**

*R: AWS Consulting Partners*
- Os parceiros de consultoria da AWS são empresas de serviços profissionais que demonstraram experiência em ajudar os clientes a projetar, arquitetar, criar, migrar e gerenciar suas cargas de trabalho na AWS. Esses parceiros têm experiência e conhecimento em computação em Nuvem AWS e podem fornecer orientação e assistência durante todo o processo de migração. Ao contratar um parceiro de consultoria da AWS, a empresa pode se beneficiar de sua experiência e aproveitar suas habilidades para planejar e executar uma migração bem-sucedida para a AWS. O parceiro pode avaliar a infraestrutura existente da empresa, projetar uma arquitetura ideal para a AWS, fornecer orientação sobre as melhores práticas e auxiliar na migração real de cargas de trabalho para a AWS.

**`57` - Uma empresa precisa estabelecer uma conexão entre dois VPCs. Os VPCs estão localizados em duas regiões diferentes da AWS. A empresa deseja usar a infraestrutura existente dos VPCs para essa conexão. Qual serviço ou recurso da AWS pode ser usado para estabelecer essa conexão?**

*R: VPC peering*
- A empresa pode usar o VPC peering para estabelecer a conexão entre dois VPCs localizados em diferentes regiões da AWS. O VPC Peering permite que as VPCs se comuniquem entre si recorrendo à infraestrutura existente. Ele é compatível com redes virtuais que tenham cidr blocks não sobrepostos. Por exemplo, as VPCs podem possuir regiões específicas de IPs e podem compartilhar serviços, aplicações e dados acessíveis entre as VPCs que participam do peering.

**`58` - Quais serviços ou recursos da AWS permitem que os usuários se conectem e implementem serviços AWS de forma programática?**

*R: AWS SDKs*
- Os SDKs de desenvolvimento de software da AWS permitem que os usuários se conectem e implementem serviços AWS programaticamente. Um SDK fornece uma biblioteca em plataforma alvo específica que permite aos desenvolvedores chamarem APIs da AWS para integrar facilmente serviços da AWS em seus aplicativos.

**`59` - Uma empresa possui uma instância única do Amazon EC2. A empresa deseja adotar uma arquitetura altamente disponível. O que a empresa pode fazer para atender a esse requisito?**

*R: Escalar horizontalmente em várias AZs*
- A empresa deve escalar horizontalmente em várias Zonas de Disponibilidade. Ao configurar a sua infraestrutura para usar várias Zonas de Disponibilidade, a empresa pode aproveitar os alto nível de redundância de várias localizações geográficas da AWS, o que minimiza o risco de saída de serviço decorrente de uma interrupção localizada.

**`60` - Qual serviço ou funcionalidade AWS uma empresa poderia usar para determinar qual unidade de negócio está usando recursos específicos da AWS?**

*R: Tags de alocação de custos (cost allocation tags)*
- A empresa deve usar as tags de alocação de custos para determinar qual unidade de negócio está usando os recursos específicos da AWS. As tags de alocação de custos são palavras-chave com informações detalhadas, que permitem ao usuário ajustar mais facilmente as despesas com serviços da AWS. As marcações de alocação permitem a organização da conta em unidades de negócio, setores e projetos.

**`61` - Qual das características são vantagens de se utilizar a nuvem AWS?**

*R: Melhoria na segurança, capacidade de computação que se ajusta sob demanda*
- Capacidade de computação ajustada sob demanda: uma das principais vantagens da Nuvem AWS é a capacidade de dimensionar a capacidade de computação para cima ou para baixo com base na demanda. Essa elasticidade permite que você ajuste seus recursos de forma rápida e fácil para atender às necessidades em constante mudança de seus aplicativos, garantindo desempenho ideal e economia de custos. Melhoria na segurança: a AWS oferece uma ampla variedade de recursos e serviços de segurança para ajudar a proteger seus dados e aplicativos. Eles fornecem controles de segurança robustos e medidas de conformidade, incluindo criptografia, gerenciamento de acesso, segurança de rede e monitoramento. A AWS possui um modelo de responsabilidade compartilhada, onde eles cuidam da segurança da infraestrutura de nuvem, e os clientes são responsáveis por proteger seus aplicativos e dados dentro da nuvem.

**`62` - Uma empresa recentemente implantou uma instância Amazon RDS em sua VPC. A empresa precisa implementar um firewall com estado para limitar o tráfego para a rede corporativa privada. Qual serviço AWS ou recurso a empresa deve usar para limitar o tráfego de rede diretamente para sua instância RDS?**

*R: Secutiry groups (grupos de segurança)*
- Os grupos de segurança são usados para controlar o tráfego de entrada e saída no nível da instância. Quando uma empresa implanta uma instância do Amazon RDS em sua VPC, ela pode associar um grupo de segurança à instância do RDS. Ao configurar as regras do grupo de segurança, a empresa pode especificar quais endereços IP ou intervalos de IP têm permissão para acessar a instância do RDS.

**`63` - Uma empresa está se preparando para lançar uma nova aplicação web que espera receber um alto volume de tráfego em um próximo evento. A aplicação é executada apenas na AWS e a empresa possui um plano de suporte da AWS Enterprise. Que recurso da AWS fornecerá orientação sobre como a empresa deve escalar sua arquitetura e suporte operacional durante o evento?**

*R: O gerente de conta técnica designado (TAM)*
- A empresa deve usar o seu gerente de conta técnica designado (TAM) para obter orientação sobre como escalar sua arquitetura e suporte operacional para a aplicação durante o evento. O TAM da empresa oferece uma única janela para os recursos de design, infraestrutura e solução da AWS, para otimizar a arquitetura durante períodos com alto volume de tráfego.

**`64` - Políticas de controle de serviço (SCPs) geram permissões para o qual das seguintes opções?**

*R: AWS Organizations*
- As políticas de controle de serviço (SCPs) gerenciam as permissões de recursos definidas dentro de uma conta individual, dentro de uma organização, ou compartilhada entre todas as contas da organização. Elas definem quais ações podem ou não ser executadas nos serviços AWS e controle como o orçamento é gasto.

**`65` - Qual dos seguintes são benefícios de migrar para o AWS Cloud? (Escolha dois.)**

*R: Resiliência operacional, agilidade de negócios*
- Migrar para o AWS Cloud oferece vários benefícios, como melhorar igualmente a resiliência e a agilidade operacionais. A resiliência operacional implica capacidade de isolamento de incidentes de menor escala dentro da organização ou mesmo entre regiões, sem afetar diretamente toda a empresa. Essa resistência pode ser reforçada pela incorporação de práticas de segurança e opções de implantação adequadas. A capacidade de aceitar mudanças e reagir de forma rápida e dinâmica é outro atributo importante para viabilizar soluções às necessidades organizacionais.
