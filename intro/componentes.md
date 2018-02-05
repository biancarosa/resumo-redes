# Hospedeiros (hosts) ou sistemas finais
Dispositivos utilizados pelo usuário final e servidores.
Acessam a internet através do ISP.

O hospedeiro envia pacotes de dados, da seguinte forma:
- Pega mensagem da aplicação.
- Quebra mensagem em pequenos pedaços, conhecidos como *pacotes*, com *L* bits de comprimento.
- Transmite o pacote pela rede de acesso a uma taxa de transmissão *R* (essa é a taxa de transmissão do canal, ou capacidade do canal, ou largura de banda do canal).

O atraso de transmissão do pacote é:

ATRASO = Tempo p/ transmitir um pacote de L bits no canal

ATRASO = L (bits) / R (bits/secs) = T secs

# Enlaces (links) de comunicação
Conectam sistemas finais entre si. A taxa de transmissão de um enlace é medida em bits por segundo e é igual a largura da banda (bandwidth)
Ex: Cabos coaxiais, fios de cobre, fibras ótimas e ondas de rádio.

O bit é propagado entre o receptor e o transmisor. O enlace físico é o que está entre o receptor e o transmissor.

Meios guiados: meios sólidos, ex: cabos (cobre, fibra, coaxial).
Meios não-guiados: sinal se propaga livremente, ex: rádio.

O par trançado (TP - Twisted Pair) são dois fios de cobre isolado. (Categoria 5: 100Mbps e 1 Gbps Ethernet / Categoria 6: 10 Gbps)

Cabo coaxial:
- Fio transporta o sinal dentro de outro fio (blindagem).
- Bidirecional.
- Banda larga (broadband) significa que tem multiplos canais em um cabo.

Cabo de fibra:
- Fibra de vidro transporta pulsos de luz.
- Transmissão ponto a ponto de alta velocidade.
- Baixa taxas de erros porque os repetidores estão mais afastados e é imune a ruído eletromagnético.

Rádio:
- Sinal transportado em ondas eletromagnéticas.
- Não há fio físico.
- Bidirecional.
- Reflexão, obstrução por objetos e interferencia são efeitos do ambiente de propagação.
- Tipos de enlace de rádio: microondas, LAN, longa distância, satélite.

# Roteadores (Comutadores de pacotes)
Responsável por encaminhar os pacotes que chegam em um de seus enlaces de comunicação de entrada para um de seus enlances de comunicação de saída.
Ex: roteadores e comutadores de camada de enlace.

# Rota percorrida até o sistema final
Pode ser chamada de rota ou caminho e é composa de enlaces de comunicação e comutadores de pacotes.

# ISP
Internet Service Providers (Serviços Provedores de Internet) são servidores que permitem o acesso à internet pelos sistemas finais. Existem vários níveis de ISPs.