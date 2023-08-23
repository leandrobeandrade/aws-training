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

### Pontos de presença (Edge Locations)

Os Edge locations são pontos espalhados pelo mundo para ajudar a acelerar a comunicação com os usuários em qualquer localidade e são amplamente utilizadas em conjunto com a CDN AWS mais conhecida como **Cloudfront**. Os Edge locations são separadas das regions, podendo-se enviar um conteúdo de dentro de uma region para uma coleção destes pontos de presença para acelerar a comunicação e entrega do conteúdo. Também executam um serviço DNS chamado `Route 53` que ajuda a direcionar corretamente requisições para os servidores web, com confiabilidade e baixa latência.