# Multiplexação - rede de circuitos
TDM - Time Division Multiplexing
FDM - Frequency Division Multiplexing

# Intensidade

dnó = dproc + denfil + dtrans +  dprop

dproc tipicamente < mseg
denfil depende do atraso
dtrans = l/r
dprop = d/s

# Trafego
intensidade de tráfego = La/R

# Vazao

vazão = Rc
vazão por conexão fim-a-fim: min(Rc,Rs,R/10)

# Camadas
aplicação: dá suporte a aplicações de rede
FTP, SMTP, HTTP
Dados

transporte: transferência de dados processo a processo
TCP, UDP
Segmento

rede: repasse (encaminhamento) de datagramas da origem até o destino
IP, protocolos de roteamento 
Pacote

enlace: transferência de dados entre elementos de rede vizinhos
PPP, Ethernet, 802.11
Enlace

física: bits “no fio”
Bits

## Camadas ISO
apresentação: permite às aplicações interpretar o significado dos dados, ex., cifragem, compressão, convenções específicas de máquina
sessão: sincronização, verificação, recuperação da troca de dados

# Virus

O Malware pode entrar nos hospedeiros através de:
vírus: infecção autoreplicante através da recepção/ execução de um objeto (ex., anexo de e-mail) 
Worms: infecção autoreplicante através da recepção passiva de um objeto que se autoexecuta

Spyware pode registrar teclas digitadas, sítios web visitados, carregar informações para sítio de coleta.

Hospedeiro infectado podem ser incluídos numa botnet, usada para gerar spams e ataques DDoS.

Negação de serviço (DoS): atacantes deixam os recursos (servidor, banda) indisponíveis para o tráfego legítimo sobrecarregando o recurso com tráfego falso

# Protocolos

## TCP
- transporte confiável
- controle de fluxo
- controle de congestionamento
- não provê garantias temporais ou de banda mínima
- orientado a conexão

## UDP
- transferência de dados não confiável
- não provê estabelecimento de conexão, confiabilidade, controle de fluxo, controle de congestionamento, garantias temporais ou de banda mínima

usado por streaming multimidia e telefonia


# HTTP

- Stateless (servidor não guarda estado)
- Total: 2RTT + tempo de transmissão
- Dois tipos de mensagem: requisição, resposta

# Request
method url version\r\n
header: value\r\n
header: value\r\n
\r\n
[body]

## Métodos 1.0
- GET, POST, HEAD

## Métodos 1.1
- GET, POST, HEAD
- PUT, DELETE

# Response

version status status_name\r\n
header: value\r\n
header: value\r\n
\r\n
data data data data data 

# HTTP/2

Mecanismos de negociação para permitir a clientes e servidores escolher o HTTP 1.1, 2, ou outros protocolos
Manutenção de compatibilidade de alto nível como HTTP 1.1
Diminuir a latência para melhorar a velocidade de carga das páginas através de:
Dar suporte aos casos de uso comuns atuais do HTTP

## Diferenças

- Mantém a maior parte da sintaxe de alto nível do HTTP 1.1 tais como: métodos, códigos de status, campos de cabeçalhos e URIs
- O que é modificado é como os dados são estruturados e transportados entre o cliente e o servidor de forma binária e não textual.
- HTTP/2 permite ao servidor enviar (push) conteúdo, i.e., enviar mais dados que os solicitados pelo cliente.
- Multiplexa os pedidos e as respostas para evitar o problema de bloqueio pelo cabeça da fila do HTTP 1.1.
- Realiza ainda um controle de fluxo e priorização dos pedidos.

# rdt - criando um protocolo

# go back n

admite janela de até n pacotes consecutivos não reconhecidos.
