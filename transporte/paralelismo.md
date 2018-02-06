# Go-back-N

1. O transmissor pode ter até N pacotes não reconhecidos no “tubo”
2. Receptor envia apenas acks cumulativos
3. Não reconhece pacote se houver falha de seq.
4. Transmissor possui um temporizador para o pacote mais antigo ainda não reconhecido
5. Se o temporizador estourar, retransmite todos os pacotes ainda não reconhecidos.

# Retransmissão Seletiva

1. O transmissor pode ter até N pacotes não reconhecidos no “tubo”
2. Receptor envia acks individuais para cada pacote
3. Transmissor possui um temporizador para cada pacote ainda não reconhecido
4. Se o temporizador estourar, retransmite apenas o pacote correspondente.