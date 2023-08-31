# AWS - Resumo Treinamento AWS

Anotações referentes ao curso AWS Cloud Practitioner na plataforma AWS Skill Builder.

## Regions AWS

Data centers com variados tipos de recursos de computação e serviços AWS sendo que cada region pode se conectar com todas as outras por meio de fibra óptica de alta velocidade. Cada region é isolada uma das outras no sentido de dependência de serviços e nenhum dado entra ou sai do ambiente desta region sem a devida permissão. A soberania dos dados é permanente na AWS e os dados estão sujeitos a les e regulamentos locais do país da region. Existem 4 pontos relacionados importantes na hora de escolher uma região:

- 1- conformidade: Dados que estejam dentro de uma região satisfazendo legislações e leis locais desta region.
- 2- proximidade: Base de clientes mais próximo da região escolhida trás maior velocidade e um menor latência.
- 3- disponibilidade: A region talvez não possuo determinado serviço nencessário contratado para o seu negócio.
- 4- preços: Depende de cargas tributárias e de impostos, quanto maior mais será custoso para operar nessa region.

### Zonas de disponibilidade (AZ - Available Zones)

São 1 data center ou um grupo de data centers com alimentação redundante, redes e conectividade, sendo que cada region consiste em várias zonas de disponibilidades ou AZ's isoladas e separadas fisicamente dentro de uma região geográfica localizada a dezenas de quilômetros de distância uma das outras. O sugerido é a execução de pelo menos 2 AZ's em uma region.

### Edge Locations - Locais de Borda

Os Edge locations são pontos espalhados pelo mundo para ajudar a acelerar a comunicação com os usuários em qualquer localidade e são amplamente utilizadas em conjunto com a **CDN AWS** mais conhecida como `Cloudfront` que os utiliza para armazenar cópias em cache de conteúdo. Os Edge locations são separadas das regions, podendo-se enviar um conteúdo de dentro de uma region para uma coleção destes pontos de presença para acelerar a comunicação e entrega do conteúdo. Também executam um serviço DNS chamado `Route 53` que ajuda a direcionar corretamente requisições para os servidores web, com confiabilidade e baixa latência.

Porém pode-se utilizar serviços AWS dentro de um data center de terceiros, esse serviço chamada-se `AWS Outposts`, que consiste basicamante na instalação e configuração de uma mini-region dentro deste data center, tendo toda a responsabilidade e propriedade da AWS, exercendo toda a operação e administração do mesmo.

## Provisionamento de recursos AWS

A forma de interagir com os serviços da AWS e por meio de **API's AWS** que servem basicamente para provisionar, configurar e gerenciar os recursos. Iniciar instâncias de um EC2 ou criar uma função Lambda por exemplo, são formas de utilização destas API's. Existem 3 formas de execução dos serviços AWS gerais que são via Console, via CLI e via SDK's.

- Console management: gerencia os recursos através de uma interface visual no site da AWS, tudo é feito manualmente.
- CLI - Command Interface Line: pelo terminal de uma máquina, cria-se scripts ou programas para chamadas as API's e automações.
- SDK - Software Development Kit: permite a interação com serviços e recursos AWS por meio de linguagens de programação.

### Elastic Beanstalk

Fornece definições de código e configurações para serviços e aplicações da Web com implantações rápidas e simplificadas.

### Cloudformation

Considera a infraestruta como código provisionando os recursos de maneira segura e repetível com reversão rápida em casos de erros, utilizando linguagens declarativas como Json ou Yaml conhecidos como templates. 

## VPC - Virtual Private Cloud

Cria uma rede de conexão privada com sessões internas isoladas conhecidas como sub-redes (subnets), cada sub-rede possui uma porção dos indereços IP's da VPC sendo estas públicas ou privadas e servem para agrupar recursos. Estas sub-redes públicas ou privadas são acessadas por meio do serviço **AWS Internet Gateway**.

- Internet Gateway público: porta de conexão pública entre o tráfego de internet público e a VPC (sub-rede pública).
- Internet Gateway privado: porta de conexão privada que permite somente tráfego autorizado entre internet e a VPC (sub-rede privada).

O Gateway privado ou VPG (Virtual Private Gateway) permite estabelecer uma conexão protegida através de uma `VPN` que criptografa todo tráfego de solicitações de internet.
Instâncias dentro das sub-redes comunicam-se entre si dentro da VPN por meio de pacotes ou unidade de dados.

### Direct Connect

Estabelece uma conexão direta utilizando fibra dedicada completamente privada entre o tráfego de rede e a VPC através de uma rede física altamente controlada, protegida e exclusiva onde só tráfego permitido trafega, diferente da VPG que apesar de protegida e criptografada trafega em uma rede pública comum.

### ACL - Lista de controle de acesso

Componente ao redor da VPC que verifica as permissões dos pacotes no fluxo de entrada e saída das sub-redes, sendo como um **firewall** virtual. Por padrão já existe uma ACL de rede comum podendo criar outras personalizadas. A **`ACL comum permite todo o tráfego de entrada e saída por padrão`** com a opção de serem modificadas estas regras, ao contrário das ACL personalizadas que todo tráfego é negado por padrão quando são criadas. Uma ACL tem o atributo **STATELESS**, ou seja, não se lembra dos pacotes e faz a verificação na entrada e saída dos pacotes. 

### Grupos de segurança

Componente dentro da VPC que controla o envio dos pacotes para instâncias dentro da mesma sub-rede ou entre sub-redes diferentes na mesma VPC, cada sub-rede já possui um **`Grupo de segurança que não permite o tráfego de entrada e saída por padrão`**, todas as portas e endereços IP's são bloqueados, podendo estas regras serem modificadas. Um Grupo de segurança tem o atributo **STATEFUL**, ou seja, se lembram dos pacotes e não fazem a verificação na entrada de retorno dos pacotes.

### Tráfego STATELESS vs STATEFUL

Exemplo de fluxo de envio e retorno de uma pacote entre sub-redes, com regras pré-definidas para o grupo de segurança permitindo o envio automaticamente:

> Envio do pacote

      1- o pacote é enviado de uma instância na sub-rede A para uma instância da sub-rede B
      2- o pacote por padrão passa pelo grupo de segurança da sub-rede A
      3- o pacote chega ao ACL que avalia (STATELESS) e deixa o pacote seguir o fluxo de saída para a sub-rede B
      4- o pacote chega a sub-rede B
      5- o pacote é avaliado (STATELESS) e passa pelo ACL da sub-rede B
      6- o pacote é avaliado e passa pelo grupo de segurança
      7- o pacote chega a instância da sub-rede B

> Retorno do pacote

      1- o pacote é enviado da instância na sub-rede B de volta para a instância da sub-rede A
      2- o pacote por padrão passa pelo grupo de segurança da sub-rede B
      3- o pacote chega ao ACL que avalia (STATELESS) e deixa o pacote seguir o fluxo de saída para a sub-rede A
      4- o pacote chega a sub-rede A
      5- o pacote é avaliado (STATELESS) e passa pelo ACL da sub-rede A
      6- o pacote por padrão passa (STATEFULL) pelo grupo de segurança
      7- o pacote chega a instância da sub-rede A

## DNS - Domain Name Service

A resolução envolve um servidor DNS que se comunica com um servidor web e converte um nome de domínio para um endereço IP.

### Route 53

Serviço AWS web de DNS roteando e conectando solicitações web à infraestrura AWS como instâncias EC2 e Load balance assim também como realizar direcionamento para fora da infraestrutura AWS. Também faz todo o gerenciamento dos registros DNS para nomes de domínio como criação e transferência de registros.

## Armazenamentos de Instância

Fornece armazenamento temporário a nível de bloco para uma instância EC2, um armazenamento em disco físico anexado ao computador host da instância, portanto tendo a mesma vida útil da instância. Quando a instância é encerrada, todos os dados no armazenamento de instâncias são perdidos.

Você pode pensar em armazenamento de blocos como um local para armazenar arquivos, um arquivo sendo uma série de bytes que são armazenados em blocos no disco. Quando um arquivo é atualizado nem toda série de blocos é substituída. Em vez disso, apenas as partes atualizadas são alteradas e isso torna o armazenamento eficiente para trabalhar com aplicações como banco de dados, softwares corporativos e sistemas de arquivos. 

A execução de uma instância a partir de um estado interrompido poderá iniciar a instância em um outro host, em que o volume de armazenamento de instâncias usado anteriormente não existe. A AWS recomenda este tipo de armazenamento para casos de uso que envolvam dados temporários de períodos de curto prazo.

### EBS - Elastic Block Store

Fornece volumes de armazenamento a nível de bloco para instâncias EC2 só que ao contrário do armazenamento de instância caso a instância EC2 seja interrompida ou encerrada, todos os dados no volume do EBS anexo permanecerão disponíveis. Como os dados alocados em volumes EBS precisam ser persistidos, é importante que seja feito backups destes dados através de **`snapshots do EBS`**. Armazena dados em uma única AZ.

Os snapshots do EBS são um backup incremental sendo que o primeiro backup de um volume copia todos os dados, já nos backups subsequentes somente os blocos de dados alterados desde o snapshot mais recente serão  salvos. Os backups complementares são diferentes dos completos que fazem uma cópia dos dados toda vez que ocorre um backup, incluindo dados que não foram alterados desde o backup mais recente.

### S3 - Simple Storage Service

Serviço AWS para armazenamento de dados simples como imagens, vídeos, sites estáticos, etc. Permitindo o armazenamento e a recuperação destes dados de forma ilimitada e em qualquer escala. Os dados são armazenados como objetos em locais chamados `buckets` ao invés de diretórios de arquivos. Sendo o tamanho máximo do objeto de 5 terabytes com permissões de acessos e proteção contra exclusão acidental. 

Há níveis de mecanismos para diferentes casos de uso de armazenamento entre dados que precisam ser armazenados com frequência versus dados retidos por vários anos. Com a utilização das políticas de ciclo de vida de armazenamento pode-se mover os arquivos por períodos entre estes serviços.

> **S3 Standard**

Fornece 11 noves de durabilidade, significa que um objeto armazenado no S3 tem uma porcentagem de 99,99999999 com probabilidade do dado permanecer intacto após um período de 1 ano sendo muito alta. Além de os dados serem armazenados em instalações AWS separadas garantindo sustentação em caso de desastres. Custo mais alto.

> **S3 Infrequent Access (S3 IA)**

Utilizado para dados acessados com menos frequência mas que exigem rapidez quando necessário, ideal para armazenamento de backups e outros dados de longo prazo. Também presente em 3 AZ's separadas. Custo baixo para armazenamento e alto para recuperação dos dados. Custo mais baixo se comparado ao S3 Standard.

> **S3 One Zone**

Fornece uma categoria boa de armazenamento para reproduzir facilmente os dados em caso de falhas. Só está presente em 1 AZ com custo mais barato.

> **S3 Intelligent-Tiering**

Monitora os padrões de acessos dos objetos, se pouco utilizados move para o SE IA, utilizado algumas vezes move os dados para S3 Standard. Cobra uma pequena taxa mensal de monitoramento e automação por objeto.

> **S3 Glacier**

Pode-se mover dados para ele ou criar cofres e depois preenchê-los com arquivos, ideal para dados armazenados por um longo prazo mas que não dependam que sejam recuperados rapidamente. Também fornece a política de `Vault Locker` podendo ser bloqueada a qualquer momento, sendo que após o bloqueio a política não poderá mais ser alterada. Custo baixo para arquivamentos de dados.

**S3 Glacier Deep Archive**

Fornece prontidão na recuperação de dados arquivados, capaz de recuperar objetos em 12 horas. Custo baixo para armazenamento de arquivos. Este serviço é otimizado para dados de arquivamento junto com o S3 Glacier.

### EFS - Elastic File Service

Sistema de arquivos escalável usado com serviços AWS e recursos locais, a medida que adiciona ou remove arquivos o EFS expande ou retrai automaticamente, dimensionando sobre demanda para petabytes sem interromper os aplicativos. Armazena dados em várias AZ's e entre elas, também podem ser caessados por Direct Connect.