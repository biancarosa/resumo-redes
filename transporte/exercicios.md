Capítulo 3

3.1-3.3

R7) Sim, serão enviados ao mesmo socket. Pra cada segmento recebido, a camada de transporte vai repassar o segmento para a camada de aplicação, informando ao processo qual o endereço IP de origem.

R8) Sim, estão sendo enviadas para o mesma porta, através de conexões diferentes, e portanto dois sockets diferentes. Por serem duas conexões abertas em endereços de origem diferentes, são dois identificadores diferentes, um para cada socket.
Pra cada conexão persistente, o servidor Web identifica os sockets através de quatro valores: (endereço ip de origem, porta de origem, endereço ip de destino, porta de destino).
Quando a camada de transporte passa esse segmento para o processo de aplicação, ela não precisa especificar o endereço IP de origem, uma vez que ele já está explícito.

3.4

R9) Precisamos introduzir numeros de sequencia em protocolos rdt para que o destinatário consiga identificar se esse pacote é uma retransmissão ou um novo pacote, assim como para identificar perdas de pacotes. Ex: Um pacote com um número de sequência muito mais avançado significa que o anterior pode ser sido perdido.

R10) Precisamos introduzir temporizadores em protocolos rdt para identificarmos casos de perda de pacote e ack ou nack perdidos. O remetente não tem como saber se um pacote foi perdido, então implementa-se um temporizador de contagem regressiva cujo objetivo é parar o processo de envio e tentar retransmitir o pacote.

R11) Mesmo sabendo o tempo que um ACK/NACK demora pra chegar, um temporizador é necessário para identificar se houve perda. A única vantagem é que, após o tempo conhecido ter passado, vai ser sabido com certeza que o pacote foi perdido.

R12) Applet (Go-Back-N)
R13) Applet (Go-Back-N)

3.5 
R14)
a) Falso.
b) Falso.
c) Verdadeiro.
d) Falso.
e) Verdadeiro.
f) Falso.
g) Falso.

R15) 
a) 20 bytes.
b) Ack Number = 90

R16) Serão enviados 3 segmentos.
Seq  = 43, ack = 80
Seq = 80, ack = 44
Seq = 44, ack = 81

3.7
a) R/2
b) Falso, o valor de ssthresh é a metade do cwnd (valor atual do congestionamento)
c)
4 * RTTfe + RTTbe + processamento

Client – Front-end  (Handshake) = RTTfe
Client – Front-end  (Requisiçao) = RTTfe
Front-End – Back-end = RTTbe + PT
Client – Front-end  (Acknowledment) = RTTfe
Client – Front-end (Fechando conexão = RTTfe
