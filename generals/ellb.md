# ELB - Elastic Load Balancing

No Balanceamento elástico de carga o tráfego pode ser direcionado.

## Elastic Load Balancing Service (Serviço de balanceamento de carga elástica)

Este serviço distribui o tráfego de aplicativos entre os serviços. O Load Balancer é um único ponto de contato para o tráfego de entrada da Web.

O ponto único de contato significa que o tráfego atinge o balanceador de carga primeiro, distribuindo a carga entre os recursos.

O balanceador aceita solicitações e as direciona para as instâncias apropriadas. Ele garante que um recurso não fique sobrecarregado e que o tráfego seja distribuído.

AWS EC2 e Elastic Load Balancing são dois serviços diferentes que funcionam bem juntos. O AWS ELB foi criado para oferecer suporte ao aumento do tráfego sem aumentar o custo por hora. O AWS ELB escala automaticamente.

## Load Allocation (Alocação de Carga)

O serviço aloca o tráfego de entrada entre os recursos disponíveis. O princípio é o mesmo nos períodos de alta e baixa demanda.

Ele irá alocar entre o que está disponível a qualquer momento.