# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## Serverless

Serverless é um serviço onde você não precisa pensar em servidores, com serverless você só precisa pensar em código e o provedor de nuvem lida com toda a infraestrutura por trás dele.

> A diferença entre EC2 e serveless

O AWS EC2 fornece instâncias de servidor virtual. Para executar o EC2, você deve fazer o seguinte:

- Provisão das instâncias do servidor virtual
- Implantação do código
- Operar e manter os servidores

> Vantagens

- Serverless não requer gerenciamento de servidor
- Pensar menos com o servidor operacional permite que você se concentre nas coisas importantes
- A abordagem sem servidor é adequada para escala
- AWS Lambda é um servidor do tipo serverless

## AWS Lambda

AWS Lambda um serviço de computação sem servidor. Este serviço permite que você execute código sem precisar pensar em servidores. Ele permite que você se concentre no que é mais importante, como fazer um ótimo aplicativo.

Você paga apenas pelo tempo de computação que usar. Pagar pelo que você usa significa que você paga apenas quando seu código está em execução. 

Ajuda a abstrair a infraestrutura na nuvem. Como resultado, reduz custos e pode ajudar a aumentar a inovação. Pode também executar o código de back-end com o AWS Lambda.

> Como funciona o AWS Lambda

- Implante seu código no Lambda
- Prepare o código para acionar um evento
- O código só é executado quando acionado
- Pague apenas quando seu código estiver em execução

    Exemplo:

        1- Você pode ver o serverless como um carro.
        2- Você liga o carro para viajar para o seu destino.
        3- Quando estiver no destino, você o interrompe.
        4- Você só usou combustível ao dirigir.

Lambda funciona da mesma maneira. O uso é sob demanda quando você executa o código.

> O AWS Lambda pode ser usado para:

- Criar e implantar aplicativos
- Monitorar e gerenciar aplicativos

## AWS Fargate - Computação sem servidor para contêineres

Ajuda a implantar e gerenciar aplicativos. A Fargate gerencia a infraestrutura para você. Você não precisa pensar no fornecimento de servidores e gerenciamento de infraestrutura ao usar o Fargate.

O AWS Fargate é uma tecnologia que pode ser usada com o Amazon ECS para executar contêineres sem a necessidade de gerenciar servidores ou clusters de instâncias do Amazon EC2. Com o Fargate, não é mais necessário provisionar, configurar ou dimensionar os clusters de máquinas virtuais para executar contêineres. Isso elimina a necessidade de escolher tipos de servidor, decidir quando dimensionar clusters ou otimizar o agrupamento de clusters.

Ao executar suas tarefas e serviços do Amazon ECS com o tipo de inicialização do Fargate ou um provedor de capacidade do Fargate, empacote a aplicação em contêineres, especifique os requisitos de sistema operacional, CPU e memória, defina as políticas de rede e do IAM e inicie a aplicação. Cada tarefa do Fargate tem seu próprio limite de isolamento e não compartilha o kernel subjacente, os recursos de CPU, os recursos de memória nem a interface de rede elástica com outra tarefa.

> Como funciona o AWS Fargate

É um serviço sem servidor. A Fargate tem um modelo de precificação pré-pago. Ele permite que você se concentre em fazer o que é mais importante: criar seus aplicativos incríveis.

> Vantagens

- Implemente e gerencie seus aplicativos, não a infraestrutura. O Fargate remove a sobrecarga operacional de escalabilidade, patches, proteção e gerenciamento de servidores
- Monitore suas aplicações por meio de integrações integradas com serviços da AWS, como o Amazon CloudWatch Container Insights. Colete métricas e logs com ferramentas de terceiros
- Melhore a segurança por meio de isolamento de workload por design. Tarefas do Amazon ECS e pods do Amazon EKS são executados em seu próprio ambiente do tempo de execução dedicado
- Pague somente pelo que usar. O Fargate escala a computação para ter uma correspondência de perto com seus requisitos de recurso especificados. Com o Fargate, não há excesso de provisionamento nem o pagamento de servidores adicionais

## ELB - Elastic Load Balancing

No Balanceamento elástico de carga o tráfego pode ser direcionado.

> Elastic Load Balancing Service (Serviço de balanceamento de carga elástica)

Este serviço distribui o tráfego de aplicativos entre os serviços. O Load Balancer é um único ponto de contato para o tráfego de entrada da Web.

O ponto único de contato significa que o tráfego atinge o balanceador de carga primeiro, distribuindo a carga entre os recursos.

O balanceador aceita solicitações e as direciona para as instâncias apropriadas. Ele garante que um recurso não fique sobrecarregado e que o tráfego seja distribuído.

AWS EC2 e Elastic Load Balancing são dois serviços diferentes que funcionam bem juntos. O AWS ELB foi criado para oferecer suporte ao aumento do tráfego sem aumentar o custo por hora. O AWS ELB escala automaticamente.

> Load Allocation (Alocação de Carga)

O serviço aloca o tráfego de entrada entre os recursos disponíveis. O princípio é o mesmo nos períodos de alta e baixa demanda. Ele irá alocar entre o que está disponível a qualquer momento.