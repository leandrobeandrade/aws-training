# Messaging

Os serviços de sistema de mensagens da AWS habilitam diferentes sistemas de software e dispositivos finais, muitas vezes usando diferentes linguagens de programação, e em diferentes plataformas – para comunicação e troca de informações. Você pode usar os serviços de sistema de mensagens da AWS para enviar e receber dados nos seus aplicativos de nuvem. A infraestrutura subjacente é provisionada automaticamente e oferece alta disponibilidade e resiliência de mensagens para dar suporte à confiabilidade dos aplicativos.

## Aplicações monolíticas e microsserviços

Os aplicativos são feitos de vários componentes. Os componentes se comunicam entre si. A comunicação pode transmitir dados, atender solicitações e manter o aplicativo em execução.

> Aplicação monolítica

Uma arquitetura com componentes fortemente acoplados pode ser chamada de aplicação monolítica. Os componentes podem ser bancos de dados, servidores, interfaces e muito mais.

Um aplicativo monolítico pode ficar vulnerável se um dos componentes falhar. Na pior das hipóteses, isso pode fazer com que todo o serviço seja desativado.

Em vez disso, seu aplicativo pode ser projetado com uma abordagem chamada microsserviços. Os microsserviços podem ajudar a manter seu serviço disponível se um componente falhar.

> Microsserviços

Os microsserviços podem ajudar a manter o serviço se um componente falhar. Os serviços podem ser mantidos porque eles se comunicam entre si e os componentes não são fortemente acoplados.

A AWS possui dois serviços que podem fazer essa integração:

- Serviço de notificação simples da AWS (AWS SNS)
- Serviço de fila simples da AWS (AWS SQS)

A diferença entre a abordagem monolítica e de microsserviços é fortemente acoplada versus fracamente acoplada. Também existem vários outros serviços para determinadas funcionalidades.

## SQS - Simple Queue Service

Serviço de enfileiramento de mensagens simples, flexível e totalmente gerenciado para trocar de modo confiável e contínuo qualquer volume de mensagens de qualquer lugar.

Ele troca e armazena mensagens entre componentes de software. O serviço adiciona as mensagens em uma fila. Usuários ou serviços pegam as mensagens da fila. Depois de processadas, as mensagens são excluídas da fila.

> Caso de uso

Crie microsserviços desacoplados altamente escaláveis, sistemas distribuídos e aplicativos sem servidor na nuvem.

> Capacidades interessantes

Escalabilidade quase infinita e habilidade de aumentar o throughput de mensagens sem pré-provisionar capacidade.

## SNS - Simple Notification Service

Serviço gerenciado de notificação por push móvel e sistema de mensagens de publicação/assinatura para entrega de mensagens com altos níveis de throughput e confiabilidade.

É um serviço de comunicação móvel e mensagens de publicação-assinatura totalmente gerenciado para entrega em massa de mensagens.

Pode ser orientado a eventos, com serviços automatizados respondendo a gatilhos. Sistemas distribuídos e microsserviços podem ser desacoplados com mensagens entre eles por meio do AWS SNS. É possível enviar mensagens de aplicativo para pessoa aos usuários com SMS, push móvel e email

> Caso de uso

Efetue o push de mensagens para uma variedade de endpoints e clientes em sistemas distribuídos, microsserviços e aplicativos sem servidor e habilite arquitetura conduzida por evento.

> Capacidades interessantes

Entrega altamente confiável de qualquer volume de mensagens a qualquer número de destinatários em vários protocolos e endpoints diferentes.

- HTTP e HTTPS
- E-mail e E-mail-JSON
- AWS SQS
- Formulários
- AWS Lambda
- SMS (dependendo da região)

> A diferença entre SQS e SNS

- SNS é um sistema de notificação, que envia mensagens para seus assinantes.
- O SQS é um sistema de filas, e os receptores precisam puxar as mensagens para serem processadas e excluídas da fila.

SNS e SQS podem funcionar bem juntos.

## MQ

Serviço gerenciado de agente de mensagens para o Apache ActiveMQ que facilita a configuração e a operação de agentes de mensagens na nuvem e possibilita a arquitetura híbrida.

> Caso de uso

Migre para um agente de mensagens gerenciado para automatizar a administração e a manutenção de software sem precisar reescrever os aplicativos existentes.

> Capacidades interessantes

Compatível com APIs e protocolos padrão do setor, incluindo JMS, NMS, AMQP, STOMP, MQTT e WebSocket.

## Amazon Pinpoint

Plataforma de envolvimento de clientes para gerenciar engajamento multicanal direcionado e transacional usando e-mail, push móvel, SMS e Lambda.

> Caso de uso

Entregue a mensagem certa ao cliente certo na hora certa para melhorar o engajamento e a conversão.

> CAPACIDADES INTERESSANTES

Análise e sistema de mensagens integrados para gerar percepções e influenciar a maneira como os clientes interagem com seus aplicativos.

## Amazon Kinesis Streams 

Serviço totalmente gerenciado e altamente escalável para coletar e processar fluxos de dados em tempo real para análise e machine learning.

> Caso de uso

Crie aplicativos personalizados e em tempo real que processam fluxos de dados usando estruturas de processamento de fluxo populares.

> Capacidades interessantes

Podem capturar e armazenar continuamente terabytes de dados por hora por meio de centenas de milhares de fontes.

## Agente de mensagens do AWS IoT

Serviço de agente de publicação/assinatura totalmente gerenciado que possibilita o envio e o recebimento de mensagens de e para o Núcleo do AWS IoT.

> Caso de uso

Envie mensagens de e para dispositivos e aplicativos AWS IoT de maneira segura usando MQTT, HTTP e WebSockets.

> Capacidades interessantes

Permite que você envie ou receba mensagens de milhões de dispositivos.

