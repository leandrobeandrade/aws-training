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

A AWS fornece uma opção de nível gratuita para mais de 100 produtos AWS. Três tipos de ofertas gratuitas diferentes estão disponíveis, conforme o produto usado.

> Sempre gratuito

      Essas ofertas não expiram e estão disponíveis para todos os clientes AWS. Por exemplo, o AWS Lambda permite um milhão 
      de solicitações gratuitas e até 3,2 milhões de segundos de tempo de computação por mês. O Amazon DynamoDB libera 25 GB
      de armazenamento gratuito por mês.

> 12 meses gratuitos

      Essas ofertas são gratuitas por 12 meses após sua data de inscrição inicial na AWS. Quantidades específicas de 
      armazenamento comum do Amazon S3, limites para horas mensais de tempo de computação do Amazon EC2 e quantidades de
      transferência de dados do Amazon CloudFront para fora são alguns exemplos.

> Versão de teste

      As versões de teste gratuitas de curto prazo começam na data em que você ativa determinado serviço. A duração de cada 
      teste pode variar de acordo com o número de dias ou a quantidade de uso do serviço. Por exemplo, o Amazon Inspector 
      oferece uma versão gratuita de 90 dias. O Amazon Lightsail (um serviço que permite que você execute servidores virtuais 
      privados) oferece 750 horas de uso gratuitas em um período de 30 dias.

### Conceitos de definições de preços

A AWS oferece diversos serviços de computação em nuvem com modelos de pagamento conforme o uso.

> Pague somente pelo que usar

      Para cada serviço, você paga exatamente a quantidade de recursos que realmente usa, sem exigir contratos de longo prazo 
      ou licenciamento complexo.

> Pague menos ao fazer reserva

      Alguns serviços oferecem opções de reserva com desconto significativo em comparação com as definições de preços da 
      instância sob demanda. Por exemplo, suponha que sua empresa use instâncias do Amazon EC2 para uma carga de trabalho que
      precisa ser executada continuamente. Você pode optar por executar essa carga de trabalho no Amazon EC2 Instance Savings
      Plans, pois o plano permite uma economia de até 72% em relação à capacidade equivalente da instância sob demanda.

> Pague menos com descontos baseados em volume, quando usar mais

      Alguns serviços oferecem definição de preço em camadas, portanto, o custo por unidade é incrementalmente menor com o 
      aumento do uso. Por exemplo, quanto mais espaço de armazenamento do Amazon S3 você usar, menos pagará por GB.

### AWS Calculadora

Permite explorar os serviços AWS e gerar uma estimativa de custo de seus casos de uso na AWS. Podendo-se organizar as estimativas da AWS por grupos que definir. Um grupo pode refletir como sua empresa está organizada, por exemplo, fornecer estimativas por centro de custo. Depois de criar uma estimativa, você pode salvá-la e gerar um link para compartilhá-la com outras pessoas.

### Exemplos de definições

- **AWS Lambda**: a cobrança é feita com base no número de solicitações das funções e no tempo necessário para serem executadas, permite um milhão de solicitações gratuitas e até 3,2 milhões de segundos de tempo de computação por mês.
- **AWS EC2**: paga-se apenas pelo tempo de computação que usar enquanto suas instâncias estão em execução. Para algumas cargas de trabalho, você pode reduzir significativamente os custos do Amazon EC2 usando instâncias spot.
- **AWS S3**: considerando os seguintes componentes de custo
    - Armazenamento: paga-se apenas pelo armazenamento usado. A taxa de armazenamento de objetos em seus buckets do Amazon S3 é cobrada com base nos tamanhos, classes de armazenamento e quanto tempo você armazenou cada objeto durante o mês.
    - Solicitações e recuperações de dados: paga-se por solicitações feitas aos seus objetos e buckets do Amazon S3.
    - Transferência de dados: não há custo para transferir dados entre diferentes buckets do Amazon S3 ou do Amazon S3 para outros serviços dentro da mesma Região AWS. No entanto, você paga pelos dados que transfere para dentro e para fora do Amazon S3, com algumas exceções. Não há custo para os dados transferidos para o Amazon S3 a partir da internet ou para o Amazon CloudFront. Também não há custo para os dados transferidos para uma instância do Amazon EC2 na mesma Região AWS que o bucket do Amazon S3.

### Painel de cobrança

Use o painel de gerenciamento de faturamento e custos da AWS para pagar sua fatura da AWS, monitorar seu uso e analisar e controlar seus custos.

- Compare o saldo atual do mês acumulado com o mês anterior e obtenha uma previsão do próximo mês com base no uso atual.
- Visualize os gastos do mês acumulado por serviço.
- Visualize o uso do nível gratuito por serviço.
- Acesse o Cost Explorer e crie orçamentos.
- Adquira e gerencie o Savings Plans.
- Publique relatórios de custos e uso da AWS.

### Cobrança consolidada

O recurso de cobrança consolidada do AWS Organizations permite que você receba uma única fatura para todas as contas AWS de sua organização. Ao consolidar, você pode rastrear facilmente os custos combinados de todas as contas vinculadas em sua organização. O número máximo de contas permitido para uma organização é quatro, mas você pode entrar em contato com o AWS Support para aumentar sua cota, se necessário.

Na sua fatura mensal, você pode revisar os encargos discriminados incorridos por cada conta. Isso permite que você tenha maior transparência nas contas da sua organização, mantendo a conveniência de receber uma única fatura mensal.

Outro benefício da cobrança consolidada é a capacidade de compartilhar preços de desconto por volume, Savings Plans e instâncias reservadas nas contas da sua organização. Por exemplo, uma conta pode não ter uso mensal suficiente para se qualificar para preços com desconto. No entanto, quando várias contas são combinadas, o uso agregado pode resultar em um benefício que se aplica a todas as contas na organização.

### AWS Budgets

No AWS Budgets, você pode criar orçamentos para planejar o uso do serviço, os custos de serviço e as reservas de instâncias. As informações são atualizadas três vezes por dia ajudando a definir com precisão a proximidade entre seu uso e os valores orçados ou limites de nível gratuito da AWS.

No AWS Budgets, você também pode definir alertas personalizados para quando seu uso exceder (ou estiver prestes a exceder) o valor orçado. Suponha que você tenha definido um orçamento para o Amazon EC2. Você deseja garantir que o uso do Amazon EC2 pela sua empresa não exceda USD 200 por mês. você pode definir um orçamento personalizado para notificação quando o uso atingir metade desse valor (USD 100). Essa configuração permite que você receba um alerta e decida como deseja prosseguir com o uso contínuo do AWS EC2.

