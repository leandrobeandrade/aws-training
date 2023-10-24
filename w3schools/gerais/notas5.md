# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## Sistema de nomes de domínio (Domain Name System)

DNS é o serviço que permite que alguém acesse seu site a partir do navegador. O DNS é como uma lista telefônica. Ele conecta o endereço IP ao nome de domínio.

## AWS Route 53

O Route 53 é um serviço da Web DNS. Ele roteia usuários finais para aplicativos de internet hospedados na AWS. O Route 53 conecta os usuários e suas solicitações aos recursos da AWS e recursos externos.

O Route 53 possui um recurso para gerenciar registros DNS. Você pode registrar novos domínios e transferi-los com o Route 53. Você pode gerenciar todos os seus nomes de domínio no Route 53.

## AWS Route 53 e AWS CloudFront

O Route 53 e o CloudFront podem ser combinados para fornecer conteúdo. 

Exemplo: Uma empresa possui 3 instâncias do EC2 em um grupo de Auto Scaling. O grupo é anexado a um Application Load Balancer.

    1- O usuário solicita dados do aplicativo do site.
    2- O Route 53 usa a resolução DNS para identificar o endereço IP.
    3- Os dados são enviados de volta para o usuário.
    4- A solicitação do usuário é enviada para o ponto de presença mais próximo por meio do CloudFront.
    5- O CloudFront se conecta ao Application Load Balancer.
    6- O Load Balancer envia o pacote para a instância do EC2.

## O que são armazenamentos de instância?

Instance Store é um volume de armazenamento que atua como um disco rígido físico. Ele fornece armazenamento temporário para a instância do Amazon EC2. Os dados em um armazenamento de instância persistem durante o tempo de vida de sua instância. Se uma instância for reinicializada, os dados no armazenamento de instâncias persistirão. Quando a instância hiberna ou termina, você perde todos os dados no armazenamento da instância.

Se uma instância iniciar a partir de um estado parado, ela poderá iniciar em outro host no qual o armazenamento de instâncias usado não existe. Recomenda-se evitar o armazenamento de dados valiosos na instância de armazenamento. Armazenamentos de instância são bons para arquivos temporários e dados que podem ser facilmente recriados.

Exemplo:

    1- A instância do AWS EC2 com um armazenamento de instância anexado está em execução.
    2- A instância do AWS EC2 foi interrompida ou encerrada.
    3- Todos os dados no armazenamento de instância anexado são excluídos.

## EBS - Elastic Block Store

O EBS é um serviço que fornece volumes de armazenamento. Você pode usar volumes de armazenamento fornecidos em instâncias do Amazon EC2. Os volumes EBS são usados para dados que precisam persistir. É importante fazer backup dos dados com snapshots do AWS EBS. Depois de criar um volume EBS, você pode anexá-lo a uma instância AWS EC2. Se a instância do EC2 parar ou for encerrada, todos os dados no volume do EBS anexado permanecerão.

### EBS Snapshot

EBS Snapshot é um backup de dados incremental. O primeiro backup de um volume faz backup de todos os dados. Cada próximo backup copia apenas um bloco de dados que foi alterado desde o último snapshot. Economiza em custos de armazenamento por não duplicar dados.

Somente os dados exclusivos desse instantâneo são removidos quando você exclui um instantâneo. Se a instância do EC2 parar ou for encerrada, todos os dados no volume do EBS anexado permanecerão.

> Comparação entre AWS EBS e AWS S3

| AWS EBS                                                                       | AWS S3                                                                        |
| --                                                                            | --                                                                            |
| Os dados são armazenados como blocos                                          | Os dados são armazenados como objetos                                         |
| O bloco de armazenamento pode ter até 16 tebibytes cada (17,6 terabytes)      | O tamanho do objeto individual pode ser de até 5.000 gigabytes (5 terabytes)  |
| Desempenho mais rápido que o AWS S3                                           | Os dados não sofre perda, degradação ou corrupção por muito tempo             |
| Os dados podem ser modificados                                                | Os dados não podem ser modificados, a menos que sejam recarregados            |

## EFS - Elastic File System

Sistema de arquivos em nuvem é um sistema de arquivos. Os dados no EFS são acessados por meio de caminhos de arquivo. Comparado ao AWS EBS, o AWS EFS salva os dados em muitas zonas de disponibilidade, a escalabilidade do AWS EFS não interrompe os aplicativos. É ideal se muitos serviços precisarem acessar os mesmos dados ao mesmo tempo.

## RDS - Relational Database Service

Banco de dados relacional em nuvem - Amazon RDS. RDS é um serviço que automatiza tarefas de banco de dados. Ele permite a execução de bancos de dados relacionais na Nuvem AWS. Ele suporta estes mecanismos de banco de dados:

- AWS Aurora
- PostgreSQLName
- MySQL
- MariaDB
- Oracle
- Servidor Microsoft SQL

Os mecanismos de banco de dados AWS RDS oferecem criptografia de dados enquanto os dados são armazenados, enviados e recebidos. O AWS RDS ajuda você a concluir tarefas administrativas mais rapidamente. Diminuir o tempo necessário para tarefas administrativas dá a você mais tempo para desenvolver os recursos do aplicativo.

## AWS DynamoDB

Banco de dados em nuvem NoSQL não relacional, sendo um banco de dados sem servidor. O DynamoDB é um serviço de alto desempenho. Como o AWS DynamoDB é um banco de dados sem servidor, você não precisa gerenciar servidores ou um sistema operacional para usá-lo.

> O que é um banco de dados não relacional?

Um dos tipos de estrutura do banco de dados não relacional são os pares chave-valor. A chave de dados representa um item e o valor de dados representa os atributos desse item. Cada item pode ter atributos diferentes. Você pode remover qualquer atributo de qualquer item a qualquer momento.

> Comparação entre AWS RDS e AWS DynamoDB

| AWS RDS                                       | AWS DynamoDB                          |
| --                                            | --                                    |
| Suporta dados complexos                       | Suporta dados estruturados simples    |
| Armazena dados em tabelas de banco de dados   | Armazena dados em documentos          |
| Mais caro que o AWS DynamoDB                  | Mais barato que o AWS RDS             |
| Mais lento que o AWS DynamoDB                 | Mais rápido que o AWS RDS             |

### AWS DynamoDB Accelerator (DAX)

É um serviço de cache na memória para AWS DynamoDB. Melhora os tempos de leitura de seus dados não relacionais. Ele melhora os tempos de resposta de milissegundos para microssegundos. É um serviço totalmente gerenciado, flexível e seguro. O Amazon DynamoDB Accelerator (DAX) é um cache de memória totalmente gerenciado e altamente disponível para o Amazon DynamoDB que oferece um ganho de performance de 10 vezes (de milissegundos para microssegundos), mesmo com milhões de solicitações por segundo. 

O DAX faz todo o trabalho pesado necessário para adicionar aceleração em memória às tabelas do DynamoDB sem que os desenvolvedores tenham de gerenciar invalidação de cache, preenchimento de dados ou gerenciamento de clusters. O DAX foi projetado para execução em um ambiente do Amazon Virtual Private Cloud (Amazon VPC).

> Vantagens

- Performance extrema
- Altamente escalável
- Totalmente gerenciado
- Facilidade de uso
- Flexível
- Seguro