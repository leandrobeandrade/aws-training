# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## Infraestrutura AWS

A infraestrutura da Nuvem AWS é criada em torno das regiões e zonas de disponibilidade da AWS. Uma região da AWS é um local físico no mundo onde temos várias zonas de disponibilidade. As zonas de disponibilidade consistem em um ou mais data centers discretos, cada um com alimentação, rede e conectividade redundantes, alojados em instalações separadas. Essas zonas de disponibilidade oferecem a capacidade de operar aplicativos e bancos de dados de produção com maior disponibilidade, tolerância a falhas e escalabilidade do que seria possível em um único data center.

> Sobre:

- 31 regiões lançadas, cada uma com várias zonas de disponibilidade (AZs)
- 99 zonas de disponibilidade
- Mais de 450 pontos de presença
- Mais de 400 locais da borda e 13 caches da borda regionais
- 34 zonas locais
- 29 zonas do Wavelength para aplicações com latência ultrabaixa
- 245 países e territórios atendidos
- 115 locais do Direct Connect

## Regions 

Existem diferentes razões para escolher uma região específica. Esses motivos podem ser:

- Regulamentos de dados
- Proximidade do cliente
- Serviço disponível
- Preços

> Regulamentações Governamentais e Governança de Dados

Alguns países não permitem que dados sensíveis sejam processados e armazenados no exterior. Sua empresa pode exigir que todos os dados da empresa residam no país.

> Proximidade do Cliente

Selecionar uma região próxima aos seus clientes pode ajudar a agilizar os serviços. Exemplo:

    - Imagine que sua empresa está sediada em Seattle e seus clientes na Noruega.
    - Você pode querer considerar ter a infraestrutura em um data center perto de você.
    - Simultaneamente, tenha os aplicativos rodando em um data center perto de seus clientes na Noruega.
    - Usar sites próximos aos seus clientes resulta em uma entrega de conteúdo mais rápida.

> Serviços de Disponibilidade de Região

Nem todos os data centers da AWS oferecem suporte a todos os serviços e recursos, mesmo com a AWS criando novos serviços o tempo todo. A disponibilização de serviços exige que a AWS crie infraestrutura nos data centers.

Como resultado, os serviços podem ainda não ter chegado a um data center perto de você, podendo-se selecionar uma região que disponibilize tal serviço para que possa ser uitlizado em específico.

## Availability Zones

Zona de Disponibilidade é um único data center ou um grupo de data centers em uma região. Em uma Zona de Disponibilidade, os data centers estão localizados a muitos quilômetros de distância um do outro. Separá-los reduz o risco de todos caírem caso ocorra um desastre na região. Simultaneamente, tenha o(s) data center(s) próximo(s) o suficiente para ter baixa latência.

Os recursos de computação em nuvem da Amazon são hospedados em vários locais no mundo todo. Esses locais são compostos por regiões da AWS, zonas de disponibilidade e zonas locais. Cada região da AWS é uma área geográfica separada. Cada região da AWS contém vários locais isolados conhecidos como zonas de disponibilidade.

A Amazon opera data centers de última geração e altamente disponíveis. Embora sejam raras, podem ocorrer falhas que afetam a disponibilidade das instâncias de banco de dados que estiverem no mesmo local. Se você hospeda todas as instâncias de banco de dados em um único local afetado por essa falha, nenhuma delas estará disponível.

> Local Zones

Uma zona local é uma extensão de uma região AWS que está geograficamente próxima de seus usuários. É possível estender qualquer VPC da região principal da AWS para as zonas locais. Para isso, crie uma sub-rede e atribua-a à zona local da AWS. Quando você criar uma sub-rede em uma zona local, sua VPC também será estendida para essa zona local. A sub-rede na zona local funciona da mesma forma que outras sub-redes na VPC.

Quando criar uma instância de banco de dados, você poderá escolher uma sub-rede em uma zona local. As zonas locais têm suas próprias conexões com a Internet e suporte no AWS Direct Connect. Assim, os recursos criados em uma zona local podem atender usuários locais com comunicações de latência muito baixa.

Usando o Local Zones, é possível colocar recursos, como computação e armazenamento, em vários locais mais próximos dos usuários. O Amazon RDS permite que você coloque recursos, como instâncias de banco de dados, e dados em vários locais. Os recursos não são replicados entre regiões da AWS, a menos que você especifique isso.

Uma zona local é representada por um código de região da AWS seguido por um identificador que indica o local, exemplo us-west-2-lax-1a.

## Edge Location - Locais de borda

O Edge Location é o data center usado para entregar conteúdo rapidamente aos seus usuários. É o site que está mais próximo dos seus usuários.

> Entrega rápida

Os pontos de presença da AWS usam um serviço chamado CloudFront. O CloudFront é usado para armazenar cópias em cache do seu conteúdo, resultando na entrega rápida do seu conteúdo.

> O que é cache?

O armazenamento em cache ajuda o software a fornecer conteúdo de maneira mais rápida e econômica. Cache é um armazenamento rápido que copia e armazena partes de dados. Os dados são armazenados em hardware que pode entregar conteúdo rapidamente, por exemplo, RAM (Random-access memory). A principal tarefa do cache é entregar o conteúdo rapidamente. Os dados são salvos na camada de hardware rápido para que não precisem usar o hardware de armazenamento lento.

O conteúdo é entregue mais rapidamente porque os dados não são mais solicitados do local principal mas sim a partir do ponto de presença, um local mais próximo do usuário.

> Como funciona o cache

O cache salva subconjuntos dos dados, tornando-os disponíveis. Depois que alguém solicita os dados, eles são copiados e armazenados no ponto de presença. Quando a próxima pessoa solicitar os mesmos dados, eles serão entregues mais rapidamente do ponto de presença mais próximo.