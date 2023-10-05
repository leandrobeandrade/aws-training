# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Conexão e Rede

A AWS com serviços de conexões fornecem aos seus clientes uma ampla rede com cobertura para praticamente todos os tipos de negócios.

O **`Virtual Private Cloud (VPC)`** é uma rede privada para implantar recursos sendo vinculado a uma região.

As **`Sub-redes (Subnets)`** são parte de uma VPC e são associadas a uma AZ, ou seja, uma AZ possui uma subnet pública (acessível a Internet, exemplo instâncias EC2) e uma subnet privada (banco de dado por exemplo).

O **`Internet Gateway`** auxilia a subnet pública a acessar a internet por meio de rotas (Route Tables).

O **`NAT Gateways`** auxilia a subnet privada a acessar a internet caso necessário. São acopladas nas subnets públicas e fazem a conexão entre a subnet privada e a internet por meio da subnet pública e suas rotas.

A **`Network Access Control List (NACL)`** é um Firewall que controla o tráfego de uma subnet, onde são acopladas, possuem regras apenas de inclusão de IP's que podem ser permitidas ou negadas, necessitando que o tráfego de retorno seja permitido (**stateless**).

Os **`Security Groups`** são como um Firewall que controla tráfego de/para uma interface de rede (ENI) ou um EC2, acopladas em instâncias apenas com regras de inclusão de IP's e outros grupos e permitem o tráfego de retorno (**statefulness**).

O **`Flow Log`** registra todo tráfego IP que passa pelas interfaces, obtém registro de fluxo de VPC, de subnet ou interfaces (instâncias EC2 ex). Auxiliam na detecção de problemas de conectividade e rede e os logs são armazenados em S3, CloudWatch e Kinesis.

O **`VPC Peering`** conecta 2 ou mais VPC's privadas usando a rede AWS.

O **`VPC Endpoints`** possibilita conectar serviços AWS usando uma rede privada AWS e não a internet pública, com maior segurança e menor latência. Possui 2 tipos o `VPC Endpoints Gateway` com conexão com S3, DynamoDB e o `VPC Endpoints Interface (ENI)` que conectam ao CloudWatch.

O **`Private Link`** cria um link de conexão entre VPC de contas diferentes, necessitando de um ELB para expor esse serviço e uma ENI para acessar este serviço, utilizando uma rede privada.

O **`Site to Site`** conecta uma on-premise VPN a AWS, via internet publica porém criptografada.

O **`Direct Connect`** conexão física entre on-premises e AWS por uma rede privada.