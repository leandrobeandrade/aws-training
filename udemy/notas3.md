# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Outros Serviços

Outros serviços gerais indispensáveis para uso na AWS.

O **`Elastic Container Service (ECS)`** lança contêineres Docker na AWS, necessita das instâncias EC2 já estarem criadas e é integrado com ELB.

O **`Fargate`** é um serviço serverless utilizado para lançar contêineres na AWS, porém com Fargate não precisamos ter a infraestrutura (EC2) criada.

O **`Elastic Container Registry (ECR)`** é serviço que armazena imagens do Docker na AWS para serem utilizadas pelo ECS ou Fargate.

O **`Lambda`** é serviço serverless que fornece funções virtuais sem gerenciamento com limites de tempo para execuções curtas de até no máximo 15 minutos, sob demanda e automaticamente escalonadas. Os preços são baseados nas ligações e durações, benefícios:

- preço pago por uso, por request e free tier (1.000.000) e computação (400.000).
- integrado com vários outros serviços AWS e linguagens Java, Python, Node...
- reativo só acontecendo quando um evento for acionado (Event-Driven).
- monitorado pelo CloudWatch.
- aumento de RAM que melhora de CPU e rede com até 10GB de RAM.

O **`Cron Job`** permite definir uma programação por período para executar determinada função Lambda, sendo executado por uma máquina Linux AMI.

O **`API Gateway`** é um serviço escalonável que permite a criação de um proxy de conexão sendo utilizado por exemplo para expor uma função Lambda ou outros serviços serverless para usuários externos. Altamente gerenciado e fornece criação, publicação, manutenção, monitoração e proteção de APIs na nuvem. Suporta protocolos Rest e WebSocket além de autenticações, limitação de chaves, etc...

O **`Batch`** é um serviço de processamento em lote em grande escala e com eficiência totalmente gerenciado. Batch job é uma funcionalidade com começo e fim, são imagens Docker e rodam em um ECS. Provisiona dinamicamente a quantidade e o tipo ideais de recursos de computação (por exemplo, CPU ou instâncias com otimização de memória) com base no volume e nos requisitos de recursos específicos dos trabalhos em lote enviados.

O **`Lightsail`** é a junção de serviços AWS em um único lugar com preços baixos e previsíveis abstraindo as complexidades destes serviços. Podendo-se configurar recursos de notificações e monitoramento. Bom para frameworks como Nginx, MEAN, Node, Lamp e CRM's como Joomla, Magento, Plesk, Wordpress, também para ambientes de desenvolvimento e testes.

