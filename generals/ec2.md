# EC2

AWS EC2 é a abreviação de AWS Elastic Cloud Compute. É um servidor virtual na Nuvem AWS facilitando o dimensionamento da capacidade para cima e para baixo.

## Vantagens

- Facilita o processo de aumentar e diminuir a capacidade
- Como resultado, você pode acessar os recursos sob demanda
- Não é necessário nenhum investimento inicial
- Você só paga pelo que precisa
- Segurança

## Uso

> 1. Inicio

    1 - Selecionar um modelo com configurações básicas como o sistema operacional, servidor de aplicativos ou aplicativos.
    2 - Decidir o tipo de instância e a configuração de hardware de sua instância.
    3 - Especificar as configurações de segurança para controlar o tráfego de entrada e saída de sua instância.

> 2. Conexão

    1 - Várias maneiras de conectar uma instância.
    2 - Programas e aplicativos têm vários métodos de conexão para trocar dados.
    3 - Os usuários podem se conectar e acessar a área de trabalho do computador fazendo login.

> 3. Uso

    1 - Uma vez conectado, você pode usar a instância.
    2 - Execute comandos para instalar software, adicionar armazenamento, copiar e organizar arquivos e muito mais.

## Tipos de instâncias EC2

Existem diferentes tipos de instância, qual usar depende das necessidades. Por exemplo, as necessidades podem ser um requisito para computação, memória ou armazenamento.

> General Purpose Instance (Instância de Propósito Geral)

A instância de propósito geral equilibra os recursos de computação, memória e rede, são melhores quando há um equilíbrio entre os recursos. Servem para muitos propósitos, como:

- Servidores de aplicativos
- servidores de jogos
- Servidores back-end para empresas
- Bancos de dados pequenos e médios

> Compute Optimized Instances (Instâncias de Computação Otimizadas)

As Instâncias Otimizadas de Computação são as melhores se houver necessidade de alta computação. Esse tipo também é bom para servidores de aplicativos, servidores de jogos e aplicativos da web.

A principal diferença é que esse tipo é ideal para necessidades de alto desempenho e computação intensiva.

> Memory Optimized Instances (Instâncias com Otimização de Memória)

Esse tipo pode fornecer cargas de trabalho de grandes conjuntos de dados rapidamente. A memória é uma área de armazenamento temporário. Ele carrega do armazenamento, mantém os dados e os processa antes que o computador possa executá-los.

O processamento permite um processo de pré-carregamento e dá à CPU acesso direto ao programa de computador. As instâncias com otimização de memória são melhores quando grandes quantidades de dados precisam ser pré-carregadas antes de executar o aplicativo.

> Accelerated Computing Instances (Instâncias de Computação Acelerada)

Este tipo usa aceleradores de hardware. Os aceleradores aumentam o processamento de dados. As Instâncias de Computação Acelerada são melhores para aplicativos gráficos e streaming.

> Storage Optimized Instances (Instâncias Otimizadas para Armazenamento)

Esse tipo é melhor quando você tem grandes conjuntos de dados no armazenamento local e são projetadas para fornecer muitas entradas o mais rápido possível. Alguns exemplos:

- Sistemas de arquivos grandes
- Armazenamento de dados
- Sistemas de transações online

## Preços

Com o AWS EC2, você paga pelo tempo de computação. Você paga apenas pelo tempo de computação que usar, oferecendo diferentes opções de preços.

> On Demand Instances (Instâncias sob demanda)

As instâncias sob demanda são mais adequadas para cargas de trabalho de curto prazo. Não requer custos iniciais ou valor mínimo na compra e são executadas até que você as interrompa. Você paga pelo que usa.

> Savings Plan (Plano de economia)

O plano de economia é um compromisso de uso por um período de 1 ou 3 anos. Comprometer-se com um período dá um preço com desconto. Se ultrapassar o orçamento, o custo vai para os preços normais (sob demanda).

> Reserved Instances (Instâncias reservadas)

As Instâncias Reservadas são usadas para reservar instâncias por um período acordado. As opções são de 1 ano ou 3 anos. Este último dá o maior desconto.

> Spot Instances (instâncias pontual)

Esse modelo de preço é melhor para cargas de trabalho com horários de início e término flexíveis, que podem sofrer interrupções. As instâncias spot podem gerar uma economia de custos de até 90%.
A razão por trás do desconto é que a AWS pode otimizar sua capacidade, oferecendo melhores preços.

> Dedicated Hosts (Hosts Dedicados)

Hosts dedicados são servidores físicos totalmente dedicados a você. Você pode usar suas licenças de software VM existentes. O host dedicado é o modelo mais caro.

## Scaling (Escalabilidade)

O dimensionamento ou escalabilidade consiste em usar apenas os recursos de que você precisa. Além disso, tenha flexibilidade para crescer livremente.

Certifique-se de ter uma arquitetura que possa lidar com mudanças na demanda. Projetar uma arquitetura escalável permite que você pague apenas pelos recursos necessários em um determinado momento.

## Auto Scaling (Escalabilidade automática)

Os servidores podem obter mais solicitações do que podem atender, muitas solicitações podem causar tempos limite e interrupções.

O AWS EC2 Auto Scaling permite adicionar ou remover instâncias do EC2 automaticamente. Automatiza a capacidade à demanda.

Existem duas abordagens:

- Dimensionamento dinâmico: responde à demanda em constante mudança
- Dimensionamento preditivo: agenda o número de instâncias com base em uma demanda prevista

O dimensionamento dinâmico e preditivo podem ser combinados para dimensionar mais rapidamente

O EC2 Auto Scaling pode ser adicionado como um buffer sobre suas instâncias.

Ele pode adicionar novas instâncias ao aplicativo quando necessário e encerrá-las quando não forem mais necessárias. Você pode configurar um grupo de instâncias.

Aqui você pode definir uma capacidade mínima de instâncias que sempre estarão em execução. O restante funcionará quando necessário. 

Você pode definir o número desejado de instâncias do AWS EC2 no grupo de escalabilidade. No entanto, a capacidade desejada é padronizada para sua capacidade mínima se não for especificada.

A última configuração é Capacidade máxima.

Aqui você define a capacidade máxima de instâncias a serem utilizadas. Os grupos de Auto Scaling permitem que você tenha um ambiente dinâmico.

Você define a capacidade mínima, o número desejado e a capacidade máxima. O grupo operará dentro da configuração e fornecerá uma arquitetura previsível e econômica.
