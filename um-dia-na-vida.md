Um dia da vida de uma página Web

1. Estudante conecta laptop a rede do campus
É necessário ter o IP do laptop, o IP do roteador e o IP do DNS.
É enviada uma solicitação DHCP Request encapsulada em UDP, encapsulada no IP, encapsulada no 802.3 Ethernet.

O quadro Ethernet é difundido na Lan (dest: FFFFFFFFFFFF) e é recebido pelo roteador que executa o servidor DHCP

Ethernet é demultiplexado para IP, que é demultiplexado para UDP que é demultiplexado para DHCP.

Servidor DHCP prepara ACK DHCP contendo IP do cliente, IP do primeiro roteador, nome e endereço IP do servidor DNS
ACK DHCP é encapsulado no servidor DHCP e é repassado para o cliente.
ACK DHCP é recebido pelo cliente.

Antes de enviar pedido HTTP, precisamos saber o IP do google.com.br.
Vamos no DNS.
Consulta DNS criada, encapsulada no UDP – IP – Ethernet.
Para enviar é necessário ter o endereço MAC do roteador.
ARP
Consulta ARP difundida, que responde ARP reply dandoo o endereço MAC da interface do roteador.
Datagrama IP contém consulta DNS que é encaminhada através do switch LAN do cliente até o primeiro roteador.
Datagrama IP é repassado da rede do campus para a rede do ISP, roteado para o servidor DNS
É demultiplexado pelo servidor DNS
Servidor DNS response ao cliente co m o endereço IP de www.google.com.br.

para enviar pedido HTTP, cliente primeiro abre um socket  TCP para o servidor web
segmento SYN TCP (passo 1 da saudação em 3 vias) inter-domínio roteado para o servidor web
servidor web responde com TCP SYNACK (passo 2 da saudação em 3 vias)
conexão TCP estabelecida!
solicitação HTTP enviada para o socket TCP
datagrama IP que contém a solicitação HTTP é encaminhado para www.google.com
servidor web responde com resposta HTTP (contendo a página web)
datagrama IP com a resposta HTTP é encaminhado de volta para o cliente
