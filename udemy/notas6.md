# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Arquitetura e ecossistema AWS

O processo de dimensionamento correto para uma instância EC2 é combinar o tamanho do tipo de instância para trabalhar com os requisitos de desempenho e capacidade com o menor custo possível. Começar pequeno e aumentar conforme exigido.

Knowledge Center - Espaço reservado para questões e perguntas mais frequentes sobre AWS.

AWS IQ - Espaço para encontrar rapidamente profissionais terceirizados parceiros AWS sobre diversos assuntos como gerenciamento de contratos, colaboração segura e faturamento integrado, por videoconferência.

AWS re:POST - Serviço Q&A par perguntas e respostas parecido com Stackoverflow.

Managed Services (AMS) - Equipe formada por especialistas que irão dar suporte de infraestrutura e de aplicações na AWS. Irão imprimir as melhores práticas para gerenciar a nuvem para a conta desejada, a disposição todos os dias 24 horas.

AWS Partner Newtork são serviços específicos oferecidos de: Tecnologia, Consultoria, Treinamento e Competência.

2:07
21. AWS Architecting & Ecosystem
259. Pillar 6: Sustainability
54] ...pilares, CAF, dimensionamento correto

Sustentabilidade: Minimização do impacto ambiental de cargas de trabalho, consciência ambiental na aquisição de produtos ou serviços, compartilhamento de recursos para minimizar gastos energéticos como água e energia elétrica.

CAF (Cloud Adoption Framework) - Whitepaper e não um serviço mas contribui para planejar de forma abrangente a transformação digital e experiência na AWS. Com recursos organizacionais e capacidades agrupadas em 6 perspectivas: Negócios, Pessoas, Governança, Plataforma, Segurança e Operações.

CAF - Transformações são formados por 5 domínios: Tecnologia, Processo, Organização, Produto.

CAF - Fases são formados por 4 tipos: Visão, Alinhamento, Lançamento, Escala.

1:49
21. AWS Architecting & Ecosystem
255. Pillar 2: Security
54] ...pilares

Segurança: Capacidade de proteger sistemas e ativos de informação, forte base de identidade, mínimo de privilégio entre contas/usuários, rastreabilidade, automatizar a segurança é uma boa prática, proteção de dados em trânsito e em repouso (criptografia), redução do acesso a dados.

Confiabilidade: Capacidade de um sistema se recuperar de interrupções na infraestrutura ou serviços, adquirir recursos computacionais e mitigar erros. Testar os procedimentos com automação, antecipar e remediar falhas.

Eficiência de Desempenho: Capacidade de maximizar o uso computacional disponível para atender a exigência. Uso de tecnologias avançadas, dimensionamento e escalabilidade, tornar-se global em minutos, serverless, simpatia mecânica.

Otimização de custos: Estabilidade para operar sistemas agregando valor comercial com menor preço possível. Pagar pelo que usar, sem gastos com data centers, medir eficiência, analisar despesas, uso de serviços em larga escala diminuindo custos.

4:02
21. AWS Architecting & Ecosystem
253. AWS WhitePapers Well-Architected Framework
54] Well-Architected Framework, princípios de design, pilares...

Baseado em alguns princípios de nuvem: para de adivinhar necessidade de capacidade, usar dimensionamento automático e sob demanda, testar o sistema em escala de produção, automatizar para facilitar arquitetura (CloudFormation) e permitir que ela evolua baseado nos dados.

Princípios de design: escalabilidade (vertical e horizontal), recursos descartáveis, automações (guiadas pelos princípios serverless), acoplamento solto, serviços e não servidores.

Excelência Operacional: Capacidade de executar e monitorar sistemas, melhorar continuamente os processos e procedimentos. Ter infraestrutura como código, boa documentação, a cada entrega fazer alterações reversíveis pequenas e frequentes. Refinar procedimentos de operações familiarizando a equipe, antecipação de falhas. Utilizado em conjunto com CloudFormation.