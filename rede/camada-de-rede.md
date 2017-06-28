# Camada de Rede

## Introdução

### Objetivo
- Transporta segmentos da estação remetente à estação receptora

### Remetente
- Recebe segmentos da camada de transporte
- Encapsula segmentos dentro de datagramas

### Destinatário (Receptor)
- Remove segmentos de dentro dos datagramas
- Entrega os segmentos para a camada de transporte

### Aonde fica essa camada
- Em todos os sistemas finais e roteadores

## Funções

### Repasse
Move pacotes de uma entrada do roteador para a saída apropriada.

### Roteamento
Determina a rota a ser seguida pelos pacotes da fonte até o destino.

### Como funciona
Algoritmo de roteamento determina o caminho fim-a-fim através da rede. A cada roteador visitado, existe uma tabela de repasse local que auxilia a encontrar o próximo link a ser visitado.

## Estabelecimento de conexão
Antes dos pacotes fluírem, dois hosts e os roteadores intermediários estabelecem uma conexão virtual.

## Serviço de cada de rede

### Orientado à conexão

#### Redes de circuitos virtuais
- Provê um serviço de camada de rede orientado para conexões.
- Caminho da-origem-ao-destino se comporta como um circuito telefônico em termos de desempenho e em ações da rede ao longo do caminho da-origem-ao-destino
- Estabelecimento de cada chamada antes do envio dos dados
- Cada pacote tem ident. de CV (e não endereços origem/dest)
- Cada roteador no caminho da-origem-ao-destino mantém “estado” para cada conexão que o atravessa
- Recursos de enlace, roteador (banda, buffers) podem ser alocados ao CV (recursos dedicados = serviço previsível)

##### Implementação
Um cirtuito virtual consiste de:
- Caminho da origem para o destino
- Números (identificadores) de circuito virtual, um número para cada enlace ao longo do caminho
- Entradas nas tabelas de repasse dos roteadores ao longo do caminho
- Roteadores guardam estado.

Um pacote que pertence a um circuito virtual carrega o número do circuito virtual (ao invés do endereço de destino).
Número do CV deve ser trocado a cada enlace e novo número do CV vem da tabela de repasse.

### Sem conexões
#### Redes de datagramas
- Provêem um serviço de camada de rede sem conexões.
- Modelo usado na internet.
- Roteadores não guardam estado.
- Pacotes são repassados utilizando endereço de destino.
- 2 pacotes entre o mesmo par origem-destino podem seguir caminhos diferentes

## Tabela de Repasse

### Busca por um endereço de destino
Ao buscar por entrada na tabela de repasse por um dado endereço de destino, usa-se o prefixo mais longo que bate com o endereço do destino.

## Roteadores

### Funções
- Rodam algoritmos / protocol de roteamento
- Repassam datagramas do enlace de entrada para o de saída

## Portas de Entrada
As portas de entrada de um roteador recebem um datagrama, procuram a porta de saída usando a tabela de rotas na memória da porta de entrada. Sua meta é completar o processamento da porta na **velocidade da linha**. Caso datagramas cheguem mais rápido do que a taxa de reenvio para o elemento de comutação, filas surgem na porta de entrada.

### Elementro (matriz) de comutação
- Transfere pacotes do buffer de entrada para o buffer de saída apropriado
- A taxa na qual os pacotes podem ser transferidos das entradas para as saídas se chama **taxa de comutação**.
- Taxa ideal para N entradas: N vezes a taxa da linha.

#### Comutação por Memória
Era utilizada por roteadores da primeira geração, que eram computadores tradicionais com comutação controlada diretamente pela CPU. O pacote era copiado para a memória do sistema e a velocidade era limitada pela largura de banda da memória (2 travessias do barramento por datagrama)

#### Comutação por barramento
Datagrama vai da memória da porta de entrada para a memória da porta de saída via um barramento compartilhado. A taxa de comutação é limitada pela largura de banda do barramento.

#### Comutação por rede de interconexão
Supera as limitações de banda dos barramentos. Redes de Bayan são um exemplo.

### Filas
Se o elemento de comutação for mais lento do que a soma das portas de entrada juntas pode haver filas nas portas de entrada.
Se o buffer de entrada transbordar (ou seja, a fila ficar tão grande a ponto de não caber mais nada no buffer de entrada), vão ocorrer perdas.
Quando um datagrama na cabeça da fila impede outros na mesma fila de avançarem, ocorre o chamado **bloqueio de cabeça de fila**.

## Porta de saída
As portas de saída recebem um datagrama e repassam para o nó de destino. O enfileiramento ocorre quando datagramas chegam mais rapidamente do que a taxa de transmissão. Um desses datagramas será escolhido para transmissão de acordo com algum algoritmo de escalonamento.

## Enfileiramento médio
Igual ao RTT típico (250 millisegundos) vezes a capacidade do link C. C = 10Gbps, buffer de 2,5Gbit. Com n fluxos, enfileiramento igual a (RTT * C) / sqrt(N).
