# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## AWS Snow Family

AWS Snow Family é um grupo de dispositivos físicos que transportam dados para dentro e fora da AWS, que podem transferir até exabytes (1 000 000 000 000 megabytes) de dados. A família AWS Snow inclui três tipos de dispositivos:

- AWS Snowcone
- AWS Snowball
- AWS Snowmobile

### AWS Snowcone

O AWS Snowcone é um dispositivo pequeno e seguro que transfere dados. É feito de 8 TB de espaço de armazenamento, 4 GB de memória e 2 CPUs.

### AWS Snowball

O AWS Snowball ou SnowBall Edge é um serviço de transporte de dados na escala de petabytes que usa dispositivos seguros para transferir grandes quantidades de dados para possui 2 tipos de dispositivos: 

| Dispositivos otimizados para `armazenamento`                                    | Dispositivos otimizados para `computação` |
|--                                                                             | -- |
| Ótimo para migrações de dados em grande escala                                | Ótimo para serviços que exigem uma grande quantidade de recursos de computação. |
| Tenha 80 TB de espaço de armazenamento em HDD para armazenamento de objetos   | Tenha 42 TB de armazenamento em HDD para armazenamento de objetos e 7,68 TB de espaço de      armazenamento SSD NVMe para volumes de blocos do AWS EBS. |
| Tenha 1 TB de armazenamento SSD para volumes de blocos                        | Trabalhe com 208 Gib de memória e 52 vCPUs. |

### AWS Snowmobile

O AWS Snowmobile move grandes quantidades de dados para a AWS que pode transferir até 100 petabytes de dados. Um petabyte é 1 000 000 000 megabytes.

## AWS Cloud Innovation

A inovação com a AWS pode melhorar seus negócios na nuvem. Os serviços da AWS ajudam você em:

- Avalie o estado atual do seu negócio
- Determine o estado em que você quer estar
- Lide com os problemas que você precisa resolver

Algumas opções para resolver seus problemas que a AWS oferece a você são:

- Aprendizado de máquina (ML)
- Inteligência Artificial (IA)
- Aplicativos sem servidor

> Aprendizado de máquina - ML

A AWS oferece uma ferramenta que ajuda você a desenvolver recursos de ML na nuvem AWS permitindo prever situações, resolver problemas complexos, analisar dados e muito mais. A AWS tem um serviço chamado **Amazon SageMaker** que reduz o tempo de desenvolvimento e a complexidade do ML.

> Inteligência Artificial - IA

IA é um software capaz de realizar tarefas humanas complexas. A AWS oferece muitos serviços baseados em IA:

- Serviço para criar chatbots de voz e texto - Amazon Lex
- Serviço que pode converter texto em fala - Amazon Polly
- Serviço que pode converter fala em texto - Amazon Transcribe
- Serviço que pode descobrir padrões de texto - Amazon Comprehend
- Serviço que pode detectar possíveis atividades de fraude online - Amazon Fraud Detection

## AWS Well-Architected Framework

AWS Well-Architected Framework é uma ferramenta que usa as melhores práticas para encontrar melhorias para seus aplicativos na nuvem. Ele ajuda você em cinco áreas:

- Excelência operacional
- Segurança
- Confiabilidade
- Eficiência de desempenho
- Otimização de custos

Essas áreas também são chamadas de cinco pilares do AWS Well-Architected Framework.

> Pilar Excelência Operacional

O pilar da excelência operacional é a capacidade de gerenciar e monitorar sistemas. Melhora os processos e procedimentos dos sistemas de suporte. Inclui:

- Fazendo mudanças pequenas e reversíveis
- Previsão de interrupções do sistema
- Executando tarefas de código
- Fazendo anotações de documentação

> Pilar de Segurança

O pilar de segurança consiste em proteger sistemas e dados. O Well-Architected Framework aplica segurança em todos os níveis. Ele protege os dados armazenados e em trânsito. Quando possível, as melhores práticas de segurança são aplicadas automaticamente.

> Pilar de Confiabilidade

O pilar da confiabilidade é a capacidade de minimizar as interrupções do sistema. Ele obtém recursos de computação conforme necessário. Implica aumentar a disponibilidade do sistema. Ele recupera automaticamente o sistema de interrupções.

> Pilar de Eficiência de Desempenho

O pilar de eficiência de desempenho é a capacidade de usar com precisão os recursos de computação. Satisfaz a eficiência sob demanda.

> Pilar de Otimização de Custos

O pilar de otimização de custos ajuda você a executar seus serviços de nuvem com os preços mais baixos. A otimização de custos realiza operações como:

- Análise dos seus custos
- Operando serviços gerenciados
- Garante que você só paga pelo que usar