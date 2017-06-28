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
