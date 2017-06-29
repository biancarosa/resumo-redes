# NAT

NAT (Network Address Translation) é uma técnica que permite que vários computadores se conectem a uma rede e acessem a Internet sem que possuir um IP único individual.
O IP do roteador é enxergado globalmente e todos os dispositivos conectados naquela rede são vistos através do IP do roteador. O problema é que as requisiçoes externas respondem ao roteador e ele precisa saber a quem entregar a resposta.

## A solução
Mapear o IP interno e a porta local do computador e gerar um número de 16 bits usando a tabela hash e escrever esse número na porta de origem. Quando a resposta chega, ele faz a operação inversa.
