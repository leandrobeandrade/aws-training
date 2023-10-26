# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## Provisionamento de recursos da nuvem AWS

Existem três maneiras principais de interagir com os serviços da AWS.

- Console de gerenciamento AWS

      É uma interface baseada na web. Ele é usado para acessar e gerenciar serviços da AWS, possui um aplicativo móvel 
      sendo melhor usada para monitorar e acessar informações de cobrança.

- Interface de linha de comando (AWS CLI)

      Interface de prompt que executa comandos e economiza tempo ao fazer solicitações de API. Permite que você controle 
      vários serviços da AWS com uma ferramenta, permite automatizar ações em serviços com scripts, sendo disponível em 
      Windows, macOS e Linux.

- Kits de desenvolvimento de software (AWS SDK)

      Os SDKs são outra opção para acessar e gerenciar os serviços da AWS, facilitando o uso dos serviços da AWS por meio de
      uma API que é ajustada à plataforma ou linguagem de programação que você usa. Os SDKs podem ser usados em aplicativos
      existentes ou novos criados na AWS. Oferecem suporte a linguagens de programação como C++, Java, .NET entre outras.

## Serviços de provisionamento em nuvem da AWS

A AWS oferece duas ferramentas gerenciadas: AWS Elastic Beanstalk e AWS CloudFormation.

### Elastic Beanstalk

O Elastic Beanstalk é um serviço de orquestração e de gerenciamento de infraestrutura da web que lida com a implantação e o dimensionamento de aplicativos e serviços da Web. Ajuda a gerenciar automaticamente a instalação, configuração, dimensionamento e provisionamento dos serviços da AWS.

Serviços da AWS gerenciados automaticamente: 

- AWS EC2 (Elastic Compute Cloud)
- Amazon S3 (Simple Storage Service)
- AWS RDS (Relational Database Service)
- Amazon DynamoDB
- Amazon SimpleDB

O Elastic Beanstalk implanta os recursos necessários para executar as seguintes tarefas:

- Ajustar capacidade
- Balanceamento de carga
- Escala automática
- Monitoramento da integridade do aplicativo

### CloudFormation

Com o AWS CloudFormation, você pode tratar sua infraestrutura como código, sendo um serviço de infraestrutura que permite criar modelos que descrevem os serviços da AWS que você deseja. Em seguida, ele trata da configuração e provisionamento dos recursos (como instâncias do Amazon EC2 ou instâncias de banco de dados do Amazon RDS) descritos no modelo.

Isso facilita porque você não precisa configurar os recursos individualmente, o CloudFormation ajuda a lidar com as dependências entre os recursos.

 Usando este serviço, você pode criar um ambiente escrevendo linhas de código, em vez de usar o Console de gerenciamento da AWS para provisionar recursos individualmente.

> Simplifique o gerenciamento da infraestrutura

Para um aplicativo web escalável que também inclui um banco de dados de back-end, você pode usar um grupo de Auto Scaling, um load balancer do Elastic Load Balancing e uma instância de banco de dados do Amazon Relational Database Service. Você pode usar cada serviço individual para provisionar esses recursos e depois de criar os recursos, você deve configurá-los para funcionarem juntos. Todas essas tarefas podem adicionar complexidade e tempo antes mesmo de você colocar seu aplicativo em funcionamento.

Em vez disso, você pode criar um modelo do CloudFormation ou modificar um existente, um modelo descreve todos os seus recursos e suas propriedades. Quando você usa esse modelo para criar uma pilha do CloudFormation, o CloudFormation provisiona o grupo de Auto Scaling, o balanceador de carga e o banco de dados para você, após a criação bem-sucedida da pilha, seus recursos da AWS estarão em funcionamento. Você pode excluir a pilha com a mesma facilidade, o que exclui todos os recursos da pilha, ao usar o CloudFormation, você gerencia facilmente uma coleção de recursos como uma única unidade.

> Replique rapidamente sua infraestrutura

Se seu aplicativo exigir disponibilidade adicional, você poderá replicá-lo em várias regiões para que, se uma região ficar indisponível, seus usuários ainda possam usar seu aplicativo em outras regiões. O desafio de replicar seu aplicativo é que ele também exige que você replique seus recursos. Você não precisa apenas registrar todos os recursos que seu aplicativo requer, mas também provisionar e configurar esses recursos em cada região.

Reutilize seu modelo CloudFormation para criar seus recursos de maneira consistente e repetível. Para reutilizar seu modelo, descreva seus recursos uma vez e, em seguida, provisione os mesmos recursos repetidamente em várias regiões.

> Controle e rastreie facilmente as alterações em sua infraestrutura

Em alguns casos, você pode ter recursos subjacentes que deseja atualizar de forma incremental. Por exemplo, você pode mudar para um tipo de instância de desempenho superior em sua configuração de execução do Auto Scaling para poder reduzir o número máximo de instâncias em seu grupo de Auto Scaling. Se ocorrerem problemas após a conclusão da atualização, talvez seja necessário reverter sua infraestrutura para as configurações originais. Para fazer isso manualmente, você não apenas precisa lembrar quais recursos foram alterados, mas também saber quais eram as configurações originais.

Quando você provisiona sua infraestrutura com CloudFormation, o modelo CloudFormation descreve exatamente quais recursos são provisionados e suas configurações. Como esses modelos são arquivos de texto, basta rastrear as diferenças em seus modelos para rastrear alterações em sua infraestrutura, semelhante à maneira como os desenvolvedores controlam as revisões do código-fonte. Por exemplo, você pode usar um sistema de controle de versão com seus modelos para saber exatamente quais alterações foram feitas, quem as fez e quando. Se a qualquer momento você precisar reverter alterações em sua infraestrutura, poderá usar uma versão anterior de seu modelo.
