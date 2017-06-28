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
