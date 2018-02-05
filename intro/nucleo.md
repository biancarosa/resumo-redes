# Núcleo de Rede

É composto por uma malha de roteadores interconectadores.

Comutação de pacotes:
1. Hospedeiros quebram as mensagens da camada de aplicação em pacotes. 
2. Pacotes são repassados de um roteador para o outro, através de enlaces no caminho da origem até o destino.
3. Cada pacote é transmitido na capacidade máxima do enlace.

- Leva L/R seg para transmitir um pacote de L-bits num enlace R bps.
- Todo pacote deve chegar ao roteador antes que possa ser transmitido no próximo enlace.
- Atraso fim-a-fim = 2L/R (desprezando o atraso de propagação)

## Funções chave

1. Roteamento
2. Repasse

### Roteamento
Determina a rota origem-destino tomada pelos pacotes através do algoritmo de roteamento.

### Repasse
Move pacotes da entrada do roteador para a saída apropriada do roteador.

## Alternativa: Comutação de Circuitos
- Recurso fim-a-fim alocados / reservados para a chamada entre origem-destino
- Recursos dedicados: sem compartilhamento
- Segmento do tipo circuito fica ocioso se não for utilizado pela chamada (sem compartilhamento)
- Usado normalmente na rede telefonica tradicional

### FDM
# TODO

### TDM
# TODO

## Comutação de pacotes versus comutação de circuitos

Comutação de pacotes permite que mais usuários utilizem a rede ao mesmo tempo. 

Para um enlace de um 1Mbit, 100kbps pra cada usuário ativo, cada usuário fica ativo 10% do tempo.

Na comutação de circuitos, serão permitidos 10 usuários.

Na comutação de pacotes, a probabilidade de termos > 10 ativos é menor do que 0,004 com 35 usuários.

P: como foi obtido o valor 0,0004?
#todo

P: o que ocorre se > 35 usuários?
#todo

A comutação de pacotes não necessita estabelecimento de conexao e é otima para dados em surtos, mas pode trazer congestionamento excessivo, que traz atraso e perda de pacotes.
