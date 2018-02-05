1. Qual é a diferença entre um hospedeiro e um sistema final? Cite os tipos de sistemas finais. Um servidor Web é um sistema final?
- Não existe diferença, são apenas nomenclaturas. Os dois estão na borda da rede. Computadores de mesa, estações de trabalho, celulares, tvs, webcams, etc são exemplos de sistemas finais. Um servidor web é um sistema final uma vez que está conectado à rede e recebe e transmite informações a outros sistemas finais.

2. A palavra protocolo é muito usada para descrever relações diplomáticas. Dê um exemplo de um protocolo diplomático.
- Como exemplo, é um protocolo diplomático não ligar diretamente para o presidente e marcar reuniões com a sua secretária.

3. O que é um programa cliente? O que é um programa servidor? Um programa servidor requisita e recebe serviços de um programa cliente?
- Tanto o programa cliente quanto o programa servidor funcionam em um sistema final, a diferença é que o programa cliente requisita e recebe informações de um programa servidor. O programa servidor não requisita serviços do programa cliente, porém recebe informações e devolve para o programa cliente.

4. Cite seis tecnologias de acesso. Classifique cada uma delas nas categorias acesso residencial, acesso corporativo ou acesso móvel.
- Dial-up (residencial, corporativo), DSL (residencial, corporativo), Cabo (residencial, corporativo), Fibra ótica (residencial, corporativo), Ethernet (residencial, corporativo), WiFi (móvel, residencial, corporativo), 3G/4G (móvel), Rádio (residencial, corporativo).

5. A taxa de transmissão HFC é dedicada ou é compartilhada entre usuários? É possível haver colisões na direção provedor-usuário de um canal HFC? Por quê?
- É compartilhada entre usuários. É possível haver colisões porque se vários usuários requisitarem algo ao mesmo tempo, a velocidade do tráfego diminui e uma resposta do provedor pode colidir com um envio de requisição.

6. Cite seis tecnologias de acesso residencial disponíveis em sua cidade. Para cada tipo de acesso, apresente a taxa downstream, a taxa upstream e o preço mensal anunciados.
- #todo

7. Qual é a taxa de transmissão de LANs Ethernet? Para uma dada taxa de transmissão, cada usuário da LAN pode transmitir continuamente a essa taxa?
- 10 Mb/s, 100 Mb/s, 1 Gb/s, 10 Gb/s. Essas taxa é dividida entre todos os usuários ativos no momento, ou seja, caso um usuário seja o único ativo, ele poderá transmitir na taxa máxima.

8. Cite alguns meios físicos utilizados para instalar a Ethernet.
- Fios de cobre trançados. Cabos coaxiais, fibras óticas e espectros de rádio.

9. Modems discados, HFC e ADSL são usados para acesso residencial. Para cada uma dessas tecnologias de acesso, cite uma faixa de taxas de transmissão e comente se a largura de banda é compartilhada ou dedicada.
- Modem discado: transmissão de 56kbps e sua largura de banda é dedicada. HFC é compartilhada e tem faixa de transmissão de 3-50Mbps. ADSL é compartilhada e sua faixa de transmissão é de 15mbps.

10. Descreva as tecnologias de acesso sem fio mais populares atualmente. Faça uma comparação entre elas.
- 3G/4G vs Wifi. O 3G/4G utiliza a rede de celular para conseguir internet, numa velocidade geralmente mais baixa.

11. Qual a vantagem de uma rede de comutação de circuitos em relação a uma de comutação de pacotes? Quais são as vantagens da TDM sobre a FDM em uma rede de comutação de circuitos?
- A rede de comutação de circuitos trabalha com sessões reservadas, ou seja, esse caminho não fica congestionado, enquanto uma de comutação de pacotes corre o risco de congestionar um caminho e atrasar a chegada do pacote. A TDM disponibiliza toda a largura de banda durante um período de tampo, sendo mais rápida do que a FDM.

12. Por que se afirma que a comutação de pacotes emprega multiplexação estatística? Compare a multiplexação estatística com a multiplexação que ocorre em TDM.
- Porque na multiplexação estatística existe a divisão da largura de banda apenas entre os usuários ativos, exatamente o que a comutação de pacotes faz. A multiplexação que ocorre em TDM reserva uma largura de banda para cada usuário, ativo ou não.

13. Suponha que existe exatamente um comutador de pacotes entre um computador de origem um de destino. As taxas de transmissão entre a máquina de origem e o comutador e entre este e a máquina de destino são R1 e R2, respectivamente. Admitindo que um roteador use comutação de pacotes do tipo armazena e reenvia, qual é o atraso total fim a fim para enviar um pacote de comprimento L? (desconsidere formação de fila, atraso de propagação e atraso de processamento)
- D = L/R1 + L/R2

14. Qual a principal diferença que distingue ISPs de nível 1 e de nível 2?
- ISPs de nível 1 se conectam a todos os ISPs de nível 1, enquanto ISPs de nivel 2 se conectam apenas a alguns ISPs de nível 1.

15. Suponha que usuários compartilhem um enlace de 2 Mbps e que cada usuário transmita continuamente a 1 Mbps, mas cada um deles transmite apenas 20 por cento do tempo. Suponha ainda que seja utilizada a comutação de pacotes.

A) Quando a comutação de circuitos é utilizada, quantos usuários podem usar o enlace?
-  Durante a comutação de circuitos, 2 usuários podem utilizar o sistema.

B) Para o restante deste problema, suponha que seja utilizada a comutação de pacotes. Por que não haverá atraso de fila antes de um enlace se dois ou menos usuários transmitirem ao mesmo tempo? Por que haverá atraso de fila se três usuários transmitirem ao mesmo tempo?
- Porque se dois ou menos usuários transmitirem ao mesmo tempo, teremos dois pacotes sendo transmitidos a 1Mbps, e o total do enlace é de 2 Mbps. Enquanto esses dois usuários estiverem transmitindo, qualquer novo pacote será enfileirado devido a capacidade máxima do enlace.

C) Determine a probabilidade de um dado usuário estar transmitindo.
- # todo

D) Suponha agora que haja três usuários. Determine a probabilidade de, a qualquer momento, os três usuários transmitirem simultaneamente. Determine a fração de tempo durante o qual a fila cresce.
- todo

16. Considere o envio de um pacote de uma máquina de origem a uma de destino por uma rota fixa. Relacione os componentes do atraso que formam o atraso fim a fim. Quais deles são constantes e quais são variáveis?
- Os atrasos constantes são os atrasos de processamento, trasmissão, propagação. O atraso variável é o atraso devido ao tamanho da fila.

17. Visite o applet "Transmission versus Propagation Delay" no Companion Website. Entre as taxas, o atraso de propagação e os tamanhos de pacote disponíveis, determine uma combinação para a qual o emissor termine de transmitir antes que o primeiro bit do pacote chegue ao receptor.
- #todo

18. Quanto tempo um pacote de 1.000 bytes leva para se propagar através de um enlace de 2.500 km de distância, com uma velocidade de propagação de 2,5 • l0Km/s e uma taxa de transmissão de 2 Mbps? Geralmente, quanto tempo um pacote de comprimento L leva para se propagar através de um enlace de distância d, velocidade de propagação s, e taxa de transmissão de R bps? Esse atraso depende cio comprimento do pacote? Esse atraso depende da taxa de transmissão?
- #todo

19. Suponha que o Hospedeiro A queira enviar um arquivo grande para o Hospedeiro B. O percurso do Hospedeiro A para o Hospedeiro B possui três enlaces, de taxas R, = 500 kbps, R ,= 2 Mbps, e R5 = 1 Mbps.
a. Considerando que não haja nenhum outro tráfego na rede, qual é a vazão para a transferência de arquivo?
b. Suponha que o arquivo tenha 4 milhões de bytes. Dividindo o tamanho do arquivo pela vazão, quanto tempo levará a transferência para o Hospedeiro B?
c. Repita os itens “a" e “b”, mas agora com R, reduzido a 100 kbps.
- #todo

20. Suponha que o sistema final A queira enviar um arquivo grande para o sistema B. Em um nível muito alto, descreva como o sistema A cria pacotes a partir do arquivo. Quando um desses arquivos chegar ao comutador de pacote, quais informações no pacote o comutador utiliza para determinar o enlace através do qual o pacote é encaminhado? Por que a comutação de pacote na Internet é análoga a dirigir de uma cidade para outra pedindo informações ao longo do caminho?
- #todo

21. Visite o applet "Queuing and Loss" no Companion Website. Qual é a taxa de emissão máxima e a taxa de emissão mínima? Com essas taxas, qual e a intensidade do tráfego? Execute o applet com essas taxas e determine o tempo que leva a ocorrência de uma perda de pacote. Repita o procedimento uma segunda vez e determine novamente o tempo de ocorrência para a perda de pacote. Os resultados são diferentes? Por quê? Por que não?
- #todo

22. Cite cinco tarefas que uma camada pode executar. É possível que uma (ou mais) dessas tarefas seja(m) realizada(s) por duas (ou mais) camadas?
- Uma camada pode garantir a entrega, pode garantir que os dados não estão corrompidos, pode ter retentativa, pode garantir que estão sendo entregues para a pessoa certa. Uma ou mais camadas podem garantir a confiabilidade dos dados, por exemplo.

23. Quais são as cinco camadas da pilha de protocolo da Internet? Quais as principais responsabilidades de cada uma dessas camadas?
- Aplicação, rede, transporte, enlace e física.
Explicação - #todo.

24. O que é uma mensagem de camada de aplicação? Um segmento de camada de transporte? Um data-grama de camada de rede? Um quadro de camada de enlace?
- É o dado na sua forma mais fragmentada (dentro dessa camada) que será repassado para a próxima camada. São pedaços do dado como um todo.

25. Que camadas da pilha do protocolo da Internet um roteador implementa? Que camadas um comutador de camada de enlace implementa? Que camadas um sistema final implementa?
- Roteador - rede, transporte, enlace
Comutador - transporte, enlace.
Sistema Final - aplicaçao, rede, transporte.

26. Qual é a diferença entre um vírus e um worm?
- #todo

27. Descreva como pode ser criado uma botnet e como ela pode ser utilizada no ataque DDoS.
- #todo
