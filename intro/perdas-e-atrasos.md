# Como ocorrem

- Pacotes enfileiram no buffer do roteador.
- Taxa de chegada de pacotes ao enlace excede a capacidade do enlace de saída.
- Pacotes enfileiram, esperam por sua vez.

# Fontes de Atraso

1. Transmissão
2. Propagação
3. Processamento do Nó
4. Enfileiramento

dnó = dproc + denfil + dtrans +  dprop

atraso de transmissão: L / R = bits/bps = s
atraso de propagação: d (comprimento do enlace físico) / velocidade de propagação no meio

Atraso de fila médio: La / R

R=largura de banda do enlace (bps)
L=compr. do pacote (bits)
a=taxa média de chegada de pacotes

La/R ~ 0: pequeno atraso de enfileiramento
La/R -> 1: grande atraso
La/R > 1: chega mais “trabalho” do que a capacidade de atendimento, atraso médio infinito!

# Vazão - throughput

vazão: taxa (bits/unidade de tempo) na qual os bits são transferidos entre o transmissor e o receptor

vazão por conexão fim-a-fim: min(Rc,Rs,R/10)