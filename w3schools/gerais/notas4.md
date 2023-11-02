# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## AWS Networking

A AWS tem muitas opções de conectividade de rede, a maneira de se conectar dependerá de sua configuração e requisitos.

### Nuvem privada virtual (VPC - Virtual Private Cloud)

A nuvem privada virtual da AWS é um serviço que permite isolar seus recursos da AWS em uma rede isolada. Os limites criados em torno dos recursos permitem que a AWS restrinja o tráfego de rede.

Além disso, permite incluir as seções da Nuvem AWS que você deseja na rede isolada, os recursos podem ser organizados em sub-redes. Uma sub-rede é uma seção na VPC que pode conter recursos específicos.

### Portal da Internet (Internet Gateway)

O tráfego público pode ser permitido para sua VPC e esta permissão é fornecida por um Internet Gateway, funcionando como uma porta entre a VPC e o tráfego da Internet. Sem o Internet Gateway, você não se pode acessar os recursos na VPC.

### Portal Privado Virtual (Virtual Private Gateway)

Um Virtual Private Gateway é usado para acessar recursos privados na VPC, possuindo camadas extras de proteção. O Virtual Private Gateway criptografa o tráfego de internet, mantendo-o protegido. É um componente que permite que o `tráfego criptografado` entre na VPC.

O Virtual Private Gateway permite que você crie uma **Virtual Private Network (VPN)** entre a VPC e a rede privada, só permitindo o tráfego de redes aprovadas. Muitas empresas usam VPNs para garantir que seu tráfego e dados estejam seguros.

### Conexão Direta (AWS Direct Connect)

O AWS Direct Connect permite fazer uma conexão privada dedicada entre o data center e uma VPC, uma conexão dedicada é ter um **link exclusivo**. O link não é compartilhado com outras pessoas, somente você e seus dados podem viajar pela conexão.

## Sub-redes (Subnets)

Uma sub-rede é uma seção de uma VPC e permite agrupar recursos, os agrupamentos podem ter diferentes necessidades de segurança ou operações, podendo-se ter sub-redes públicas e privadas.

### Sub-redes públicas

As sub-redes públicas têm recursos que o público pode acessar, por exemplo, a página da sua empresa, como aws.com.

### Sub-redes privadas

As sub-redes privadas possuem recursos que só podem ser acessados por meio da rede privada. Por exemplo, bancos de dados contendo dados de clientes.

As sub-redes públicas e privadas podem se comunicar entre si por meio de canais seguros.

### Tráfego de rede em uma VPC

Os dados solicitados são enviados como um pacote, sendo um pacote um empacotemento de dados enviados por uma rede ou pela Internet. Ele entra na VPC por meio de um Gateway da Internet e antes de entrar em uma sub-rede, ele verifica as permissões.

Verificando permissões como:

- Quem enviou o Pacote?
- Como o pacote se comunicará com os recursos na sub-rede
- Listas de controle de acesso à rede (ACL's)

### ACL's (Access Control List)

ACL é um firewall que controla o tráfego, tanto de entrada quanto de saída, controlando o tráfego no nível da sub-rede. A ACL verifica e controla os pacotes, se o pacote estiver na lista de aprovados, ele passará, no entanto, se eles não estiverem na lista, o acesso será negado.

> Filtragem de pacotes sem estado (Stateless packet filtering)

As ACLs fazem a filtragem Stateless Packet, elas não têm memória e esquecerão o pedido depois de verificados. O trabalho delas é verificar os pacotes que entram e saem, usando as regras definidas para aprovar ou negar o acesso.

### Grupos de segurança

Um grupo de segurança é um firewall que controla o tráfego de entrada e saída, sendo um recurso específico para uma instância AWS EC2. A configuração padrão nega todo o tráfego de entrada e permite todo o tráfego de saída. Você precisa adicionar novas regras para alterar essa configuração.

> Filtragem de pacotes com estado (Statefull packet filtering)

Grupos de segurança fazem filtragem de pacotes com monitoramento de estado, eles se lembram das ações que fizeram com os pacotes no passado.

### Configuração

Tanto as ACLs como os grupos de segurança podem ser configurados, o que significa adicionar regras personalizadas para o tráfego.