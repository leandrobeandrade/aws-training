# AWS - Anotações Curso Udemy

Anotações referentes ao curso [Ultimate AWS Certified Cloud Practitioner](https://www.udemy.com/share/103a093@qP42hME1G1UUc8yWpjZ5Y-ClltzgbSLLCtxkCYFIguDx8A6K8ydl8WaA_ZRyD7B2/) na plataforma Udemy.

## Cloud Computing

É a entrega sob demanda de poder de computação, armazenamento de banco de dados, aplicações e outros recursos de TI. Os tipos de modelos de cloud são distribuídos em segmentos:

- Private Cloud: Nuvem privada, com serviços privados por exemplo rackspace.
- Public Cloud: Nuvem pública que oferece serviços gerenciados para uso público por exemplo Microsoft Azure, Google Cloud e AWS.
- Hibrid Cloud: Nuvem híbrida que mescla infraestrutura local (on-premise) utilizando serviços da nuvem.

Possuindo **`5`** característica principais e **`6`** vantagens sobre computação fora da nuvem.

### 5 Características

- On-demand self service: Uso sob demanda e sem a necessidade de gerenciamento de terceiros.
- Broad network access: Acesso a uma rede ampla de recursos e serviços.
- Multi-tenancy: Multi locação e pooling de recursos, todos clientes usam os mesmos recursos.
- Rapid elasticity and scalability: Rápida escalabilidade e elasticidade baseados na demanda.
- Measured services: Serviços medidos com pagamentos medidos e somente pelo que usamos.

### 6 Vantagens

- Trocar negociações de despesas capitais (CAPEX) por despesas operacionais (OPEX), aluguel de hardware.
- Benefícios de enormes economias de escala, devido ao tanto de clientes utilizando e alimentando AWS em escala.
- Parar de adivinhar capacidade, através de dimensionamento dos recursos.
- Agilidade e velocidade sem bloqueios ou esperas, tudo em apenas poucos instantes.
- Parar com custo de execução e manutenção de data centers.
- Alcançe global em minutos fornecido pela infraestrutura global AWS.

Possibilitando assim a computação em nuvem a resolução de problemas como:

- `flexibilidade:` mudar os recursos quando necessário.
- `custo efetivo:` pagamos pelo uso (pay-as-you-go).
- `escalabilidade:` adicionar mais recursos quando necessário.
- `elasticidade:` escalonamentos verticais e horizontais.
- `disponibilidade:` alta disponibilidade de recursos e tolerâncias a falhas.
- `agilidade:` desenvolvimento, testes e lançamento de serviços e produtos rapidamente e globalmente.

### Tipos de Computação em nuvem

- Infrastructure as a Service (IaaS)
    - Fornece blocos de construção para TI.
    - Fornece rede, computação, espaço de armazenamento de dados em forma bruta.
    - Alto nível de flexibilidade.
    - Fácil entendimento de como migrar da TI tradicional para a nuvem.
    - AWS EC2, Google Cloud Plataform, Azure, Rackspace, Digital Ocean, Linode.
- Plataform as a Service (PaaS)
    - Elimina a necessidade da organização gerenciar a infraestrutura subjacente.
    - Foco na implementação de um produto/serviço ao invés de pensar em como entregar.
    - Elastic Beanstalk, Heroku, Google App Engine, Windows Azure.
- Software as a Service (SasS)
    - Produto completo gerenciado e executado pelo provedor do serviço.
    - Muitos serviços AWS como Rekognition, Cognito, Lex e outros como Gmail, Dropbox, Zoom, etc...

Na AWS paga-se pelo uso, computação paga pela computação utilizada, armazenamento pago pelos dados armazenados e rede paga pelo tráfego de saída da AWS, o tráfego de entrada dos dados é gratuito.

## IAM - Identity and Access Management

Os usuários IAM acessam a AWS usando um nome de usuário e uma senha. Uma política do IAM **(Policies)** é uma entidade que, quando anexada a uma identidade ou recurso, define suas permissões. O relatório de credenciais do IAM lista todos os usuários da sua conta e o status de suas diversas credenciais. A outra ferramenta de segurança IAM é o **IAM Access Advisor** que lista as permissões de serviço concedidas a um usuário e quando esses serviços foram acessados pela última vez.

O **`Security Token Service (STS)`** permite a criação de privilégios temporários e limitados para usuário, podendo-se configurar o tempo de expiração.

O **`Cognito`** fornece um banco de dados aos usuários de aplicações web e mobile com controle de acesso simples.

O **`Directory Services`** são diretórios AWS que se conectam com terceiros como AWS Managed Microsoft AD (Active Directory) ou AD Connector, funciona como um proxy que vai redirecionar a solicitação da AWS para o AD Local, ambos possuem autenticação MFA. Também tem o Simple AD que é um diretório simples na nuvem AWS e não pode ser associado a um AD Local.

O **`IAM Identity Center`** antigo Single Sign-On, é um login para todas as contas AWS na organização.

## EC2

Um dos serviços mais essênciais apresentado pela AWS, sendo do tipo `IaaS` que fornece aluguel de máquinas virtuais, armazenamento de dados em unidades virtuais ou em volumes **(EBS)**, distribuição de carga através das máquinas **(ELB)**, dimensionamento de serviços utilizando grupos de auto-scaling **(ASG)**.

Fornece a escolha de máquinas com os 3 principais sistemas operacionais: Windows, Linux e MacOS, assim como a potência de computação, quantidade de núcleos necessárias, quanto de espaço de armazenamento, placa de rede e firewall. A instância é inicializada (bootstrapping) por um script chamado `Userdata` que é utilizado apenas na primeira inicialização. O **`AMI (Amazon Machine Image)`** fornece a personalização de uma instância EC2 pública através de customização da instância por meio de configurações de sistemas operacionais e especificação de regions.

Os **`grupos de segurança`** ficam fora do EC2 e controlam todo tráfego de entrada e saída das instâncias EC2 contendo regras de permissões referenciando IP's ou outros grupos de segurança. São como um firewall que regulam os acessos as portas, os IP's autorizados e o controle dos tráfegos de entrada e saída. Um grupo pode ser anexado a várias instâncias e uma instância pode conter vários grupos. São bloqueados para uma VPC/Region, todo tráfego de entrada é bloqueado e todo tráfego de saída é autorizado por padrão.

> O processo de dimensionamento correto para uma instância EC2 é combinar o tamanho do tipo da instância para trabalhar com os
  requisitos de desempenho e capacidade com o menor custo possível. Começar pequeno e aumentar conforme exigido. Aumentar a 
  escala é fácil, por isso começar sempre aos poucos.

Tipos de aquisição de instâncias EC2:

- **`On Demand`:** Paga pelo uso, tem custo mais alto, porém sem custos antecipados ou a longo prazo, cargas de trabalho curta e ininterrupta.
- **`Instâncias Reservadas`:** Desconto de 72% em relação a on demand, reservas de período de 1 a 3 anos, cargas de trabalho estáveis. A instância reservada conversível tem apenas 66% de desconto.
- **`Saving Plans`:** Uso de longo prazo com desconto de 72% comparada as instâncias reservadas.
- **`Instâncias Spot`:** Desconto de 90% em relação a on demand, porém podendo perde-lá se ultrapassar o custo devido a ter que calcular um preço máximo de uso. São mais baratas, boas para cargas resilientes a falhas e não para trabalhos críticos.
- **`Hosts Dedicados`:** Host físico, custo mais caros de todos. Software com licenças próprias ou empresa com forte necessidade regulatória.
- **`Instâncias Dedicadas`:** Executadas em hardware físico com compartilhamento com outras instâncias.
- **`Capacidade Reservada`:** Capacidade reservada de instâncias específicas em uma AZ por qualquer duração de temppo.  

O **`Elastic Block Store (EBS)`** são drivers de rede que podem ser anexados nas instâncias EC2 ou NÃO, permitindo persistir dados mesmo depois da instâncias estarem encerradas. Sendo o EBS vinculado a uma AZ específica com 30GB grátis em free tier, útil para failovers, porém pode-se copiar um EBS a outra AZ com um EBS instantâneo (backup) ou EBS Snapshot levando de 24 a 72 horas para cópias.

O **`Amazon Machine Image (AMI)`** são personalizações de uma instância EC2 pública que pode ter a customização da instância por meio das configurações, assim como os sistemas operacionais e especificação de regions.

O **`Image Builder`** automatiza a criação de máquinas virtuais ou imagens de contêineres. É um pipeline automatizado para criação, manutenção, validação, testes, compartilhamento e implantação de imagens Linux ou 
Windows para uso na AWS e no local (on-premises).

O **`Instance Store`** é utilizado para melhorar o desempenho de I/O com boa taxa de transferência. Ou seja, desempenho de disco extremamente rápido que é perdido quando a instância EC2 for encerrada, bom para armazenamento temporário.

O **`Elastic File System (EFS)`** é um sistema de arquivos de rede ou NFS, pode ser montado em centenas de instâncias EC2 por vez, funcionando em diversas AZ's com máquinas Linux, sendo altamente disponível, escalável e bastante caro, cerca de 3x mais que o EBS, pagando pelo uso sem o planejamento de capacidade. O **`EFS-IA (Infrequent Access)`** é uma classe de armazenamento otimizada para arquivos com pouca frequência de acesso com custo de 92% menor que o EFS.

O **`Amazon FSx`** torna fácil e econômico o lançamento e execução de sistemas de arquivos populares totalmente gerenciados pela AWS. Ele vem em duas ofertas: FSx for Windows File Server (usado para aplicativos de negócios) e FSx for Lustre (usado para computação de alto desempenho).