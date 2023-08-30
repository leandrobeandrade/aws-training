# AWS - Resumo Treinamento AWS

Anotações referentes ao curso AWS Cloud Practitioner na plataforma AWS Skill Builder.

## AWS CloudWatch

Serviço web que permite monitorar e gerenciar métricas e ações de alarme de acordo com os dados dessas métricas. Usa métricas para representar os pontos de dados para seus recursos. Os serviços AWS enviam as métricas ao CloudWatch, em seguida, o CloudWatch usa essas métricas para criar automaticamente gráficos que mostram como o desempenho mudou ao longo do tempo.

### Alarmes CloudWatch

Com o CloudWatch, você pode criar alarmes que executam ações automaticamente se o valor da métrica ultrapassar ou for inferior a um limite predefinido. Os alarmes do CloudWatch são integrados ao **SNS**. Você pode criar todos os tipos de alarmes personalizados para métricas de todos os tipos para recursos da AWS.

### Painel CloudWatch

Permite o acesso a todas as métricas de seus recursos em um único local. Por exemplo, você pode usar um painel do CloudWatch para monitorar a utilização da CPU de uma instância do Amazon EC2 ou o número total de solicitações feitas para um bucket do Amazon S3. Você pode até personalizar painéis separados para diferentes fins comerciais, aplicativos ou recursos.

## AWS CloudTrail

O AWS CloudTrail registra as chamadas de API realizadas na sua conta. As informações gravadas são identidade do chamador da API, hora da chamada da API, endereço IP de origem do chamador da API e muito mais. Pode-se usar chamadas de API para provisionar, gerenciar e configurar recursos AWS, com o CloudTrail, pode-se visualizar um histórico completo de atividades do usuário e chamadas de API de seus aplicativos e recursos. 

Normalmente, os eventos são atualizados no CloudTrail dentro de 15 minutos após uma chamada de API, podendo-se filtrar os eventos especificando a hora e a data em que uma chamada de API ocorreu, o usuário que solicitou a ação, o tipo de recurso envolvido na chamada de API e muito mais.

### CloudTrail Insights

Recurso opcional permitindo que o CloudTrail detecte automaticamente atividades de API incomuns em sua conta AWS. Por exemplo, o CloudTrail Insights pode detectar que mais instâncias do Amazon EC2 foram executadas recentemente em sua conta em relação ao usual. Em seguida, você pode revisar os detalhes completos do evento para determinar quais ações precisa executar a seguir.

## AWS Trusted Advisor

O AWS Trusted Advisor é um serviço web que inspeciona seu ambiente AWS e faz recomendações em tempo real de acordo com as práticas recomendadas da AWS, compara suas descobertas com as práticas recomendadas da AWS em cinco categorias expostas no Painel Trusted Advisor: **otimização de custos**, **desempenho**, **segurança**, **tolerância a falhas** e **limites de serviço**. Para as verificações em cada categoria, o Trusted Advisor oferece uma lista de ações recomendadas e recursos adicionais para saber mais sobre as práticas recomendadas da AWS.

Para cada categoria:

- marca de verificação verde indica o número de itens para os quais não foram detectados problemas.
- triângulo laranja representa o número de investigações recomendadas.
- círculo vermelho representa o número de ações recomendadas.

As orientações feitas pelo AWS Trusted Advisor podem beneficiar sua empresa em todos os estágios da implantação. Por exemplo, você pode usar o AWS Trusted Advisor para ajudar enquanto cria novos fluxos de trabalho e desenvolve novos aplicativos, usá-lo enquanto faz melhorias contínuas em aplicativos e recursos existentes ou buckets do Amazon S3 com permissões de acesso aberto.

## Preços e suporte


