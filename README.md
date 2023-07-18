# AWS

![image](https://github.com/leandrobeandrade/aws-training/assets/24658433/f0201903-4dfc-44e1-87d8-4a4ba615779a)

> Tipos de Cloud - do mais básico para o mais completo

- Iaas -> Infrasctructure-as-a-service (Utiliza uma infraestrutura já pronta para ser utilizada como serviço)
- Paas -> Plataform-as-a-service (Utiliza uma plataforma já pronta para ser utilizada como serviço)
- Saas -> Software-as-a-service (Utiliza uma aplicação já pronta para ser utilizada como serviço)

> Termos de Cloud

- Public -> S3 por exemplo
- Hybrid -> app publico e banco de dados privado por exemplo
- Private -> .gov por exemplo

> AWS Services

- Computação -> Amazon EC2, etc...
- Armazenamento -> S3 (Amazon Simple Storage Service), etc...
- Banco de Dados -> AWS DynamoDB, AWS RDS, AWS Redshift, etc...
- Redes -> AWS API Gateway, AWS Cloud Wan, AWS VPN, etc...
- Análises -> AWS Athena, AWS CloudSearch, AWS EMR, etc...
- Machine Learning -> AWS Forecast, AWS Kendra, AWS Lex, AWS Omics, etc...
- Segurança Geral -> AWS Cognito, AWS Detective, AWS GuardDuty, AWS Inspector, etc...
- [todos os serviços](https://aws.amazon.com/pt/products/?aws-products-all.sort-by=item.additionalFields.productNameLowercase&aws-products-all.sort-order=asc&awsf.re%3AInvent=*all&awsf.Free%20Tier%20Type=*all&awsf.tech-category=*all)

> Modelo de Responsabilidade Compartilhada

- [modelo de responsabilidade](https://aws.amazon.com/pt/compliance/shared-responsibility-model/)

> EC2 - Elastic Compute Cloud



- controle
- segurança
- integrado com outros serviços AWS
- baixo custo

> ECS - Elastic Container Service

Serviço de orquestração de contêineres

- implantação rápida, confiável e eficiente
- independe de ambiente 

> S3 - Simples Storage Service

- Não tem limites de dados dentro do S3
- 1 objeto upado pode ter no máximo 5TB
- Garante durabilidade de 99.999
- Garante disponibilidade de 99.95 até 99.99

> AMI - Amazon Machine Image

Imagens privadas (minha) e públicas (AWS fornece e empresas terceiras utilizam)

> Scaling up

Escala nas próprias instâncias, causando upgrade dos recursos das mesmas

> Scaling Out

Escala as instâncias criando novas instâncias com os mesmo recusrsos da padrão chamada launch template

> Auto Scaling (faz parte do scaling out)

Cria novas instâncias ou diminui o número das instâncias automáticamente através de policies inseridas dentro do auto scaling group

> Load Balancer (trabalha em conjunto com auto scaling)

Distribui as requisições para os servidores conhecendo suas disponibilidades, caso a instância esteja com algum problema isso é detectado pelo LB e a requisição é redirecionado para outro servidor

- ALB (Application Load Balancer) -> trabalha na camada 7 no modelo osi, mais inteligente
- NLB (Network Load Balancer) -> trabalha na camada 4 no modelo osi, mais rápido

#  Billing e Pricing

- pay as you go -> pague conforme utiliza (final do mês)
- pay for you use -> pague de acordo com o que utiliza
- pay less as you use more -> pague menos, se utilizar mais
- pay less as you reserved -> pague recursos reservados
- CAPEX -> Capital expenditure (Paga antes de usar, valor fixo e mais caro)
- OPEX -> Operation expenditure (Paga quando utiliza)
- Budget x Cost Explorer -> Orçamento antes do uso(Budget), Relatório da conta após uso(Cost Explorer)

# Security 

> Artifact

Disponível no console, é um portal de autoatendimento para recuperação de artefatos de auditoria que oferece aos clientes acesso sob demanda à documentação de conformidade e aos acordos da AWS.

> Responsability model (parte do cliente)

Banco de dados seguro, webserver dentro de EC2 tem que ter garantia assim como instalação de SO, configurações seguras de network e firewall , entre outros

> AWS WAF e Sield

- WAF -> Web application firewall, analisa os potenciais riscos na camada 7
- Shield -> Escudo - detecta aumento de volume e identifica se é genuíno ou por ataques

> Security Services

- Inspector -> agente instalável em uma instância que inspeciona os ambientes EC2
- Trusted Advisor -> trabalha em real time e identifica a estrutura AWS utilizada
- Cloud Trail -> monitora API calls ou AWS console

> Athena x Macie

- Athena -> fornece pesquisa através de standard SQL para pegar dados de um S3 que recebe dados de um EC2
- Macie -> fornece pesquisa através de marchine learning para pegar geralmente dados confidenciais e sensíveis de um S3 através de natural language proccess (NLP), só funciona na região

# Cloudformation

> Beneficios

- Infra code -> controle, versionamento, visualizar mudanças
- custo -> tag, custo estimado, por padrão gratuito desde que esteja em free tier

> code template

Crias as máquinas e serviços em 2 ou 3 minutos por linguagens declarativas como JSON e Yaml

# Termos
On-Premises Deployment -> Implantação local ou implantação de nuvem privada
