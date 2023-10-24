# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Conexão e Rede

A AWS com serviços de conexões fornecem aos seus clientes uma ampla rede com cobertura para praticamente todos os tipos de negócios.

O **`Virtual Private Cloud (VPC)`** é uma rede privada para implantar recursos sendo vinculado a uma região.

As **`Sub-redes (Subnets)`** são parte de uma VPC e são associadas a uma AZ, ou seja, uma AZ possui uma subnet pública (acessível a Internet, exemplo instâncias EC2) e uma subnet privada (banco de dado por exemplo).

O **`Internet Gateway`** auxilia a subnet pública a acessar a internet por meio de rotas (Route Tables).

O **`Network Address Translation (NAT) Gateways`** auxilia a subnet privada a acessar a internet caso necessário. São acopladas nas subnets públicas e fazem a conexão entre a subnet privada e a internet por meio da subnet pública e suas rotas.

A **`Network Access Control List (NACL)`** é um Firewall que controla o tráfego de uma subnet, onde são acopladas, possuem regras apenas de inclusão de IP's que podem ser permitidas ou negadas, necessitando que o tráfego de retorno seja permitido (**stateless**).

Os **`Security Groups`** são como um Firewall que controla tráfego de/para uma interface de rede (ENI) ou um EC2, acopladas em instâncias apenas com regras de inclusão de IP's e outros grupos e permitem o tráfego de retorno (**statefulness**).

O **`Flow Log`** registra todo tráfego IP que passa pelas interfaces, obtém registro de fluxo de VPC, de subnet ou interfaces (instâncias EC2 ex). Auxiliam na detecção de problemas de conectividade e rede e os logs são armazenados em S3, CloudWatch e Kinesis.

O **`VPC Peering`** conecta 2 ou mais VPC's privadas usando a rede AWS.

O **`VPC Endpoints`** possibilita conectar serviços AWS usando uma rede privada AWS e não a internet pública, com maior segurança e menor latência. Possui 2 tipos o `VPC Endpoints Gateway` com conexão com S3, DynamoDB e o `VPC Endpoints Interface (ENI)` que conectam ao CloudWatch.

O **`Private Link`** cria um link de conexão entre VPC de contas diferentes, necessitando de um ELB para expor esse serviço e uma ENI para acessar este serviço, utilizando uma rede privada.

O **`Site to Site`** conecta uma on-premise VPN a AWS, via internet publica porém criptografada.

O **`Direct Connect`** é uma conexão física entre on-premises e a AWS por uma rede privada.

O **`Customer Gateway`** estabelece uma VPN site to site no data center local e um Virtual Private Gateway na VPC.

O **`Client VPN`** cria uma conexão entre um computador usando OpenVPN e a rede privada AWS no data center local, através de uma conexão site to site e uma VPC no meio.

O **`Transit Gateway`** conexão de peering entre milhares de VPC e o sistema local com uma conexão estrela hub-and-spoke. Com o gateway centralizando e distribuindo as conexões.

## Segurança e Conformidade

Segurança na AWS é a maior prioridade. À medida que as organizações adotam a escalabilidade e a flexibilidade da nuvem, a AWS as ajuda a transformar segurança, identidade e conformidade em facilitadores de negócios essenciais. Comformidade ajuda você a compreender os controles robustos implementados na AWS para segurança e proteção de dados na nuvem. A conformidade é uma responsabilidade compartilhada entre a AWS e o cliente, e você pode visitar o Modelo de Responsabilidade Compartilhada.

Os **`DDoS`** são ataques de negação de serviço distribuído através de vários servidores, sobrecarregando a aplicação/servidor, impossibilitando o acesso/uso.

O **`Shield`** prove segurança contra ataques DDoS gratuitamente atuando nas camadas 3 e 4, já o AWS Shield Advanced prove segurança premium com suporte 24/7 custando $3.000.

O **`Web Application Firewall (WAF)`** funciona como um filtro de rede baseado em regras (ACL's) e atua na camada 7. Auxilia contra **ataques de SQL injection**. Ajuda a proteger aplicativos web ou APIs contra explorações comuns da web que podem afetar a disponibilidade, comprometer a segurança ou consumir recursos excessivos. O CloudFront e Route 53 também auxiliam na proteção contra os ataques.

O **`Network Firewall`** protege em todos os aspectos a VPC desde a camada 3 até a 7 com o tráfego em qualquer direção.

O **`Penetration Testing (Pen Testing)`** fornece testes contra ataques de penetração na própria infraestrutura para testes de segurança, sem a necessidade de aprovações prévias ao seguintes serviços AWS: EC2, API Gateways, NAT Gateways, ELB, AWS RDS, CloudFront, AWS Aurora, funções Lambda e Elastic Beanstalk.

A **`Criptografia`** possui dois tipos, em repouso (dados arquivados em disco rígido, RDS, S3 Glacier Deep Archieve, etc...) e em trânsito (on-premises para AWS, EC2 para o DynamoDB, etc...).

O **`Key Management Service (KMS)`** é um serviço gerenciado pela AWS para chaves sem fornecer acesso a elas, apenas dizemos quem podemos acessar as chaves.

O **`Hardware Security Modules (HSM)`** é um serviço que a AWS gerencia o software para criptografia e fornece apenas o hardware e a conta é quem gerencia as chaves.

O **`AWS Certificate Manager (ACM)`** provisiona, gerencia, implanta certificado SSL ou TLS (publico e grátis ou privado pago), fornecendo criptografia in-flight para sites acopladas nos ELB, com renovações dos certificados automáticas.

O **`Secrets Manager`** são segredos criptografados e utilizados para rotacionar alterações de senhas.

O **`Artifact`** é um portal de acesso para relatórios sob demanda de conformidade (ISO, PCI, SOC) e contratos AWS (BAA, HIPPA).

O **`GuardDuty`** auxilia na descoberta de ameaças de forma inteligente, utiliza aprendizado de máquina e detecta anomalias utilizando dados de terceiros como base.

O **`Inspector`** executa avaliações de segurança automatizadas para serviços como EC2, Lambda, ECR.

O **`Config`** audita e registra a conformidade dos recursos gravando as configurações e mudanças ao longo do tempo, é por região e em conjunto com SNS para notificar problemas.

O **`Macie`** serviço gerenciado para dados e segurança, utiliza aprendizado de máquina para descobrir dados sensíveis (PII - personally identifiable information) na AWS.

O **`Security Hub`** ferramenta de segurança central que gerencia várias contas AWS automatizadamente em um painel, agrega alertas para diferentes serviços e ferramentas de terceiros.

O **`AWS Detective`** analisa, investiga e identifica rapidamente a causa raiz dos problemas de segurança ou suspeitas utilizando aprendizado de máquina e gráficos de back-end.

O **`AWS Abuse`** serviço para denuncias de abuso de recursos ou de propósitos legais como Spam, DoS, DDos, etc...

O **`Root User`** é basicamente o usuário raiz que tem privilégios totais na conta. Não recomendado utilizar diariamente.

O **`IAM Access Analyzer`** é um serviço que demonstra quais recursos estão sendo compartilhados externamente. Definindo uma zona de confiança em toda a organização e qualquer coisa fora desta zona que tentar usar qualquer recurso será constatada.

## Machine Learning

A AWS oferece o conjunto mais amplo e aprofundado de serviços de inteligência artificial e de machine learning (ML) e infraestrutura de nuvem de apoio.

- **Rekognition**: Reconhece objetos, pessoa, textos, cenas, imagens e vídeos usando aprendizado de máquina.
- **Transcribe**: Converte a fala em texto através de ASR (automatic speech recognition), podendo-se remover partes como informações pessoais (PII) e também traduzir para idiomas diversos.
- **Polly**: Converte texto em fala.
- **Translate**: Tradução de linguagem natural para um determinado idioma.
- **Lex + Connect**: Reflete a tecnologia Alexa, serve para criar bots e conectar centers.
- **Comprehend**: Serviço serverless para processamento de linguagem neural (PLN).
- **SageMaker**: Para devs ou cientistas de dados que queiram desenvolver modelos de aprendizado de máquina.
- **Forecast**: Fornece previsões de planejamentos e demandas, 50% melhor que análises.
- **Kendra**: Pesquisa de documentos com extração de informações por aprendizado de máquina.
- **Personalize**: Recomendações personalizadas sobre produtos, marketing.
- **Textract**: Extrator de textos e documentos digitalizados, tabelas, imagens, etc...
