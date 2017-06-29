# Protocolo IP

## Framentação e remontagem
Cada enlace de rede tem um MTU (max transmission unit), sendo o MTU o maior tamanho possível de quadro nesse enlace. Com isso, o datagrama IP pode ser dividido e virar vários datagramas, sendo remontado apenas no destino final.

## Endereço IP
O endereço IP é um endereço de 32 bits que identifica uma interface. Um roteador típico possui múltiplas interfaces. Um computador típico possui uma ou dois interfaces (ethernet e Wi-Fi).

## CIDR
CIDR: Classless InterDomain Routing (Roteamento Interdomínio sem classes)

## DHCP
DHCP: Dynamic Host Configuration Protocol
- Discover
- Offer
- Request
- ACK / NACK

O DHCP também retorna:
- endereço do próximo roteador para o cliente
- nome e endereço IP do servidor DNS
- máscara de rede (indicando as porções do endereço que identificam a rede e o hospedeiro) 
