# Anotações gerais

Anotações referentes ao [Tutorial AWS Cloud](https://my-learning.w3schools.com/tutorial/aws) no site W3Schools.

## Modelo de responsabilidade compartilhada (Shared responsibility model)

Segurança e conformidade constituem uma responsabilidade compartilhada entre a AWS e o cliente. Esse modelo compartilhado pode auxiliar a reduzir os encargos operacionais do cliente à medida que a AWS opera, gerencia e controla os componentes do sistema operacional do host e a camada de virtualização, até a segurança física das instalações em que o serviço opera. O cliente assume a gestão e a responsabilidade pelo sistema operacional convidado (inclusive atualizações e patches de segurança), por outros softwares de aplicativos associados e pela configuração do firewall do grupo de segurança fornecido pela AWS. 

Os clientes devem examinar cuidadosamente os serviços que escolherem, pois suas respectivas responsabilidades variam de acordo com os serviços utilizados, a integração desses serviços ao seu ambiente de TI e as leis e regulamentos aplicáveis. A natureza dessas responsabilidades compartilhadas também oferece a flexibilidade e o controle do cliente necessários para a implantação. Esta distinção entre responsabilidades é denominada normalmente como segurança **"da"** nuvem versus segurança **"na"** nuvem.

## Responsabilidade da AWS

A responsabilidade da AWS é a segurança da nuvem que gerencia todas as camadas de infraestrutura, as camadas são:

- Centros de dados (data centers)
- Hardware e software
- Virtualização 
- Rede

## Responsabilidade de um cliente

A responsabilidade dos clientes é a segurança de tudo o que eles fazem na nuvem AWS.

- O cliente têm total controle sobre o seu conteúdo
- O cliente gerencia serviços, software e acesso aos dados da AWS

Diferenças de responsabilidade:

| AWS                           | Cliente                                   |
|--                             |--                                         |
| Locais de borda               | Proteção de tráfego de rede               |
| Zonas de disponibilidade      | Criptografia do lado do servidor          |
| Regiões                       | Criptografia de dados do lado do cliente  |
| Infraestrutura global da AWS  | Configuração de sistemas operacionais     |
| Hardware                      | Configuração de rede                      |
| Rede                          | Configuração de firewall                  |
| Banco de dados                | Gerenciamento de plataforma               |
| Armazenamento                 | Gerenciamento de aplicativos              |
| Computação                    | Gerenciamento de identidade               |
| Software                      | Gerenciamento de acesso                   |
|                               | Dados do cliente                          |

## IAM - AWS Identity and Access Management

O AWS IAM também é chamado de AWS Identity and Access Management. Ele ajuda você a gerenciar com segurança os recursos e serviços da AWS. Os recursos do IAM são:

- Usuário raiz da conta da AWS
- Usuários IAM
- Política IAM
- Grupos IAM
- Funções do IAM
- Autenticação multifator

Ao combinar os recursos do IAM, você tem a flexibilidade de configurar acessos operacionais e de segurança específicos.

### AWS Account Root User (Usuário raiz)

O usuário raiz da conta da AWS é criado quando você inicia uma conta da AWS, sendo acessada pelas credenciais da conta da AWS (e-mail e senha) tendo acesso total a todos os recursos de contas e serviços da AWS. Algumas das boas práticas são:

- Evite usar o usuário root para tarefas diárias
- Use-o para criar IAM com permissões para criar outros usuários
- Use-o apenas para as tarefas específicas do usuário raiz

### IAM Users (Usuário comum)

O usuário do IAM representa uma entidade (pessoa ou aplicativo) que interage com os recursos e serviços da AWS. O usuário do IAM é feito de credenciais e um nome e é criado sem permissões por padrão. O usuário root pode conceder permissões ao usuário IAM sendo recomendável criar um usuário do IAM para cada indivíduo.

### IAM Policies

As políticas do IAM são documentos que negam ou permitem ações para recursos e serviços da AWS, personalizam o acesso do usuário aos recursos e serviços da AWS. Você pode conceder apenas as permissões de que cada usuário precisa.

### IAM Groups

Uma coleção de usuários do IAM é chamada de grupo do IAM. A política do IAM atribuída ao grupo do IAM concede permissões a todos os usuários do IAM desse grupo.

### IAM Roles (Funções)

A função do IAM fornece acesso temporário a serviços ou recursos. Antes que uma função do IAM possa ser atribuída, o usuário, serviço ou aplicativo do IAM deve ter permissão para alternar as funções. É melhor para casos em que o acesso temporário precisa ser concedido.

### Multi-factor Authentication (MFA)

A autenticação multifator é uma autenticação em várias etapas que pode fornecer mais de um formulário de autenticação, sendo uma camada extra de segurança. Pode vir na forma de um código de segurança que é enviado para o seu dispositivo móvel ou um e-mail.

## Organizations AWS

O AWS Organizations é um contêiner para suas contas da AWS que vem com um usuário root da organização por padrão. Ele permite que você gerencie as permissões das contas da sua organização. As permissões nas organizações da AWS são controladas por políticas de controle de serviço (SCPs). Os SCPs permitem que você restrinja recursos e serviços da AWS para cada conta.

### Organizational Units

Unidades organizacionais (OUs) são grupos de contas na organização da AWS. OUs são usadas para gerenciar contas com permissões iguais ou semelhantes com mais facilidade. A política de permissão de OU é aplicada a todas as contas de OU.

## AWS Cloud Compliance

Você pode automatizar seus processos de conformidade e auditoria por meio dos melhores serviços da categoria compatíveis com a escalabilidade e segurança da infraestrutura da AWS, de acordo com o modelo de responsabilidade compartilhada. Assim, você é capaz de automatizar processos, fiscalizar de maneira contínua a postura de conformidade de todos os seus recursos da AWS, e coletar evidências automaticamente para melhorar a sua operacionalidade de auditoria e a geração de relatórios internos e o monitoramento em curso em tempo real.

### AWS Artifact

AWS Artifact é um serviço que fornece acesso a relatórios de conformidade e segurança da AWS sob demanda, consiste em AWS Artifact Reports e AWS Artifact Agreements. Existem muitos regulamentos e relatórios que você pode encontrar nos artefatos da AWS.

> Contratos de artefatos da AWS (Artifact Agreements)

Contratos de artefatos da AWS são acordos sobre o uso de determinados tipos de informações, os tipos de informações são usados em todos os serviços da AWS. Ele pode gerenciar contratos de contas individuais ou todos os contratos de contas da AWS Organization.

> Relatórios de artefatos da AWS (Artifact Reports)

O AWS Artifact Reports fornece relatórios de conformidade e informações sobre a responsabilidade de conformidade com relação a determinados padrões. Os AWS Artifact Reports estão sempre atualizados.

### Customer Compliance Center - Centro de Conformidade do Cliente

O Customer Compliance Center é um grupo de recursos que ajuda você a aprender mais sobre a conformidade da AWS. Ele pode ajudá-lo com questões de conformidade e auditar a lista de verificação de segurança. Você também pode descobrir como outras empresas resolveram seus problemas de conformidade no Centro de Conformidade do Cliente. 

## Denial-of-Service Attacks - DoS

Ataques de negação de serviço (DoS) são um esforço para tornar um aplicativo ou site inacessível, causando uma inundação excessiva de dados que sobrecarrega um aplicativo ou uma rede de sites. O ataque DoS vem de uma única fonte.

## Distributed Denial-of-Service Attacks - DDoS

Ataques distribuídos de negação de serviço (DDoS) vêm de diferentes fontes. Assim como o DoS, o DDoS tenta tornar um aplicativo ou site inacessível. O ataque pode vir de mais de um atacante ou de um único atacante que usa bots que são computadores infectados que inundam automaticamente seu aplicativo ou um site com tráfego excessivo. A AWS fornece um AWS Shield para reduzir os efeitos de ataque DoS e DDoS em seu aplicativo ou site.

## AWS Shield

O AWS Shield oferece proteção contra ataques DoS e DDoS, fornecendo proteção padrão e avançada. A proteção padrão do AWS Shield protege todos os usuários da AWS sem nenhum custo e o AWS Shield Advanced é um serviço pago que fornece detalhes do ataque e pode minimizar os efeitos de ataques mais complexos.

## AWS KMS

O AWS KMS também é conhecido como AWS Key Management Service, garante a segurança dos dados do seu aplicativo com chaves criptográficas. Uma chave criptográfica é uma sequência de caracteres que pode ser usada para criptografar ou descriptografar dados. A criptografia de dados está bloqueando os dados e a descriptografia de dados está desbloqueando os dados. Você está no controle total de suas chaves, podendo permitir que os usuários do IAM gerenciem as chaves do AWS KMS.

## AWS WAF

O AWS WAF também é conhecido como AWS Web Application Firewall que monitora as solicitações de rede do seu aplicativo. Ele pode permitir ou bloquear o tráfego de rede utilizando ACL (lista de controle de acesso à web).

## AWS Inspector

O Amazon Inspector ajuda você a melhorar a segurança dos aplicativos, assim como a melhorar a conformidade dos aplicativos. Ele verifica o aplicativo em busca de versões de software e outras vulnerabilidades, oferecendo um relatório de todos os problemas de segurança e recomendações de soluções para seu aplicativo.

## AWS GuardDuty

AWS GuardDuty é um serviço de detecção de ameaças que detecta ameaças para recursos e infraestrutura da AWS monitorando constantemente a atividade na rede. Assim como o AWS Inspector, ele relata ameaças encontradas e corrige recomendações.