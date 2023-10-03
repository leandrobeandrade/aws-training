# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Outros Serviços

Outros serviços gerais indispensáveis para uso na AWS.

O **`Elastic Container Service (ECS)`** lança contêineres Docker na AWS, necessita das instâncias EC2 já estarem criadas e é integrado com ELB.

O **`Fargate`** é um serviço serverless utilizado para lançar contêineres na AWS, porém com Fargate não precisamos ter a infraestrutura (EC2) criadas.

O **`Elastic Container Registry (ECR)`** é serviço que armazena imagens do Docker na AWS para serem utilizadas pelo ECS ou Fargate.

O **`Lambda`** é serviço serverless que fornece funções virtuais sem gerenciamento com limites de tempo para execuções curtas de até no máximo 15 minutos, sob demanda e automaticamente escalonadas. Os preços são baseados nas ligações e durações, benefícios:

- preço pago por uso, por request e free tier (1.000.000) e computação (400.000).
- integrado com vários outros serviços AWS e linguagens Java, Python, Node...
- reativo só acontecendo quando um evento for acionado (Event-Driven).
- monitorado pelo CloudWatch.
- aumento de RAM que melhora de CPU e rede com até 10GB de RAM.

O **`Cron Job`** permite definir uma programação por período para executar determinada função Lambda, sendo executado por uma máquina Linux AMI.