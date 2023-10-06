# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Arquitetura na AWS

Uma boa arquitetura na nuvem segue algumas premissas e princípios de design indispensáveis para o seu sucesso, como parar de adivinhar a capacidade e dimensionar conforme a demanda, testar o sistema em escala de produção, automatização para facilitar a experimentação arquitetônica (ClodFormation), permitir que a arquitetura evolua por exemplo caso haja mudanças nos requisitos, arquitetura baseada em dados, escalabilidade (vertical e horizontal), recursos descartáveis (criação e exclusão de instâncias EC2), automações (guiadas pelos princípios serverless), acoplamento solto com quebra em aplicações menores, serviços e não servidores.

O **`Well-Architected Framework`** auxilia os clientes em todos os ciclos da criação da arquitetura na AWS, sendo baseado em 6 pilares: 

- Excelência Operacional
> Capacidade de executar e monitorar sistemas, melhorar continuamente os processos e procedimentos. Ter infraestrutura como
  código, boa documentação, a cada entrega fazer alterações reversíveis pequenas e frequentes. Refinar procedimentos de 
  operações familiarizando a equipe, antecipação de falhas. Utilizado em conjunto com CloudFormation.

- Segurança
> Capacidade de proteger sistemas e ativos de informação, forte base de identidade, mínimo de privilégio entre contas ou 
  usuários, rastreabilidade, automatizar a segurança é uma boa prática, proteção de dados em trânsito e em repouso 
  (criptografia), redução do acesso a dados.

- Confiabilidade
> Capacidade de um sistema se recuperar de interrupções na infraestrutura ou serviços, adquirir recursos computacionais e mitigar erros. Testar os procedimentos com automação, antecipar e remediar falhas.

- Eficiência de Desempenho
> Capacidade de maximizar o uso computacional disponível para atender a exigência. Uso de tecnologias avançadas, 
  dimensionamento e escalabilidade, tornar-se global em minutos, serverless, simpatia mecânica.

- Otimização de Custos
> Estabilidade para operar sistemas agregando valor comercial com menor preço possível. Pagar pelo que usar, sem gastos com 
  data centers, medir eficiência, analisar despesas, uso de serviços em larga escala diminuindo custos.

- Sustentabilidade
> Minimização do impacto ambiental nas cargas de trabalho, consciência ambiental na aquisição de produtos ou serviços, c
  ompartilhamento de recursos para minimizar gastos energéticos como água e energia elétrica e emissão de carbono.

O **`Well-Architected Tool`** é uma ferramenta on-line na AWS que serve como auxílio para por em prática os pilares do Well-Architected Framework.

O **`CAF (Cloud Adoption Framework)`** é um Whitepaper e não um serviço, que contribui para planejar de forma abrangente a transformação digital e experiência na AWS. Com recursos organizacionais e capacidades agrupadas em 6 perspectivas:

- **Business**: prove clareza dos benefícios da adoção da nuvem AWS nos negócios.
- **People**: serve como uma ponte entre tecnologia e pessoas, pessoas capacitadas com maior performance na nuvem.
- **Governance**: orquestra iniciativas na nuvem, maximizando os ganhos e minimizando os riscos.
- **Plataform**: prove uma plataforma híbrida, escalável com modernização para cargas de trabalho existentese e inovações.
- **Security**: prove confidencialidade, integridade e disponibilidade dos dados.
- **Operations**: garante que os serviços em nuvem sejam oferecidos em um nível que atenda os requisitos do negócio.

O CAF também é sustentado por 5 domínios:

- `Tecnologia`: uso da nuvem para migrar e modernizar infraestrutura legada, aplicações e dados.
- `Processo`: digitalização, automatização e otimização das operações.
- `Organização`: reimaginação e reorganização do modelo operacional com métodos ágeis.
- `Produto`: reimaginação do modelo de negócio afim de criar novas propostas de valor, de produto e de serviço.

Além do CAF possuir 4 fases para sua completa adoção: 

- Visão: indentifica possibilidades e oportunidades com base na transformação digital.
- Alinhamento: identifica sobre as 6 perspectivas do CAF um plano de ação.
- Lançamento: criação de um produto/serviço piloto para demonstração.
- Escala: expande o piloto obtendo ganho no tempo para comercializações.

## Ecossistema AWS

O **`Knowledge Center`** é um espaço reservado para questões e perguntas mais frequentes sobre AWS.

O **`AWS IQ`** é um espaço para encontrar rapidamente profissionais terceirizados parceiros AWS para diversos assuntos como gerenciamento de contratos, colaboração segura e faturamento integrado, funciona por videoconferência.

O **`AWS re:POST`** é um serviço Q&A para perguntas e respostas parecido com Stackoverflow.

O **`Managed Services (AMS)`** uma equipe formada por especialistas que irão dar suporte de infraestrutura e de aplicações na AWS. Irão imprimir as melhores práticas para gerenciar a nuvem para a conta desejada, a disposição todos os dias 24 horas.

O **`AWS Partner Newtork (APN)`** é um serviço específico oferecido acerca dos assuntos de tecnologia, consultoria, treinamento e competência.