# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## AWS CloudTrail

AWS CloudTrail registra ações dentro do seu ambiente AWS, registrando chamadas de API em sua conta como uma trilha ou rastro. O CloudTrail fornece um histórico completo da atividade do usuário e chamadas de API em seus recursos. Exemplo de registros de dados:

- Identidade
- Tempo
- Endereço de IP

### Eventos do CloudTrail

CloudTrail pode ser usado para criar eventos, os eventos são configurados para entender o que aconteceu, permitindo filtrar e localizar eventos específicos. Os eventos podem, por exemplo, nos dizer o que?, quem? quando? Como? O evento fornece uma visão situacional.

O CloudTrail tem um recurso chamado `CloudTrail Insights` que permite a detecção de atividades de API incomuns em sua conta por meio de automação.

## Cloud Inspection Service - AWS TrustedAdvisor

Serviço de inspeção de nuvem, o TrustedAdvisor verifica sua conta, avalia e recomenda você a seguir as práticas recomendadas da AWS, é um serviço de recomendação em tempo real baseado na web que verifica sua conta e compara suas descobertas com as seguintes categorias:

- Otimização de custos
- Desempenho
- Segurança
- Tolerância ao erro
- Limites de serviço

TrustedAdvisor retorna uma lista de ações recomendadas, também fornecerá recomendações de material de aprendizado para entender melhor as práticas recomendadas da AWS.

### AWS TrustedAdvisor Dashboard

TrustedAdvisor tem um painel baseado na web com acesso pelo Console de gerenciamento da AWS. O painel fornece uma visão geral das verificações concluídas e dos resultados por categoria.

- Verificação verde: sem problemas
- Triângulo laranja: investigações recomendadas
- Círculo vermelho: ações recomendadas

## AWS CAF - Cloud Adoption Framework

O AWS CAF é uma estrutura que orienta você na migração de aplicativos para a nuvem com seis áreas de foco:

- Negócios
- Pessoas
- Governança
- Plataforma
- Segurança
- Operações

As áreas de foco do AWS CAF também são chamadas de perspectivas.

> Perspectiva de Negócios

A Perspectiva de Negócios trata de justificar o investimento e garante que os objetivos de negócios e de TI atendam ao investimento. As funções nas Perspectivas de Negócios são:

- Proprietários de orçamento
- Gerentes de negócios
- Gerentes financeiros
- Partes interessadas da estratégia

> Perspectiva das Pessoas

A Perspectiva de Pessoas avalia habilidades, requisitos e funções em sua organização, trata de garantir que você tenha as habilidades, competências e processos corretos para migrar para a nuvem. O processo de avaliação ajuda você a implementar as mudanças ou melhorias necessárias. Os papéis nas Perspectivas de Pessoas são:

- Gestores de pessoas
- Recursos humanos (RH)
- Pessoal (staffing)

> Perspectiva de Governança

A Perspectiva de Governança trata de minimizar o risco e simultaneamente, maximizar o valor do negócio ajudando você a entender as lacunas. Dando a você uma compreensão de como garantir processos e habilidades da equipe. Os papéis nas Perspectivas de Governança são:

- Diretor de Informação (CIO)
- Arquitetos corporativos
- Analistas de negócios
- Gerentes de programa
- Gerentes de portfólio

> Perspectiva da Plataforma

A perspectiva da plataforma ajuda você a implantar novas soluções em nuvem, também ajuda a migrar a carga de trabalho local para a nuvem. As funções nas Perspectivas da Plataforma são:

- Diretor de Tecnologia (CTO)
- Arquitetos de soluções
- Gerentes de TI

> Perspectiva de Segurança

A Perspectiva de Segurança garante que os objetivos de segurança da organização sejam atendidos. A Perspectiva de Segurança inclui objetivos para:

- Agilidade
- Visibilidade
- Auditabilidade
- Controle

As funções nas Perspectivas de Segurança são:

- Diretor de Segurança da Informação (CISO)
- Analistas de segurança de TI
- Gerentes de segurança de TI

> Perspectiva de Operações

A Perspectiva de Operações trata da administração do negócio e garante que as operações comerciais atendam às expectativas. Inclui negócios ano a ano, trimestre a trimestre e dia a dia. Ele ajuda a definir as mudanças necessárias para a adoção bem-sucedida da nuvem. As funções nas Perspectivas de Operações são:

- Gerentes de operações de TI
- Gerentes de suporte de TI

### AWS CAF Strategies

As estratégias de migração são planos que ajudam você a mover seus aplicativos para a nuvem. Existem seis estratégias mais comuns que você pode implementar para a migração de aplicativos:

- Rehosting -> rehospedagem é um processo de mover aplicativos sem fazer nenhuma alteração neles.
- Replatforming -> nova plataforma também chamado de lift, tinker e shift. É um processo de mover aplicativos com otimizações de nuvem.
- Refactoring -> refatoração ou reestruturação também é chamada de re-arquitetura. É um processo de alteração da base/núcleo e/ou ambiente do aplicativo. Ele ajuda no dimensionamento de aplicativos, no desempenho e no desenvolvimento adicional.
- Repurchasing -> recompra é um processo de mudança do tipo de negócio. Ele move seu aplicativo para um modelo de software como serviço (SaaS) de um modelo tradicional.
- Retaining -> reter envolve manter aplicativos de negócios cruciais. Pode incluir aplicativos que requerem refatoração antes da migração.
- Retiring -> processo de remoção de aplicativos desnecessários.