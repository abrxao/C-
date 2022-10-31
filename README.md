Na primeira questão do roteiro, era nos fornecida uma tabela verdade e em seguida era pedido para montarmos no MUX 74LS151 um circuito que tinha saídas equivalentes com a da tabela. Sem muita dificuldade e com auxilio do datasheet conectei as saídas A, B e C, respectivamente nas portas S0, S1 e S2. Conectei também a porta Z o led que nos dará informação sobre a passagem de corrente. E por ultimo verifiquei as portas que habilitariam as saídas pedidas na tabela verdade que foram as portas L0, L2, L4 e L6.

Na segunda questão, era nos apresentado um problema com um multiplexador duplo 4x1 74LS153
que consistia em conectar nas entradas 13, 12, 11 e 10, respectivamente, clock de 0.1HZ, 1HZ, 10HZ e 1KHZ. Também foram conectadas as saídas A e B nas entradas 2 e 14, essas portas eram responsáveis por informar qual frequência iria sair na porta 9. 

Tabela verdade
A  B     S    
0  0   0.1HZ
0  1    1 HZ
1  0    10HZ
1  1    1KHZ

Agora vamos usar o DEMUX 74LS155, conectando da entrada 15 a frequência de 1HZ, nesse C.I temos uma curiosidade que a entrada de data é em uma porta NAND junto com um a porta 14, chamada de “strobe”, que quando ativada faz que a saída fique disponivel. E nas portas 13 e 3, eram conectadas as saídas A e B, que ficam responsáveis por controlar em qual porta a frequência sairá.  

Tabela verdade
A  B      S    
0  0    porta 9
0  1    port 10
1  0    port 11
1  1    port 12

Por ultimo, era pedido para conectar a saída do MUX na entrada no DEMUX. E com isso, podemos escolher qual informação passará e endereçaremos a saída dela no DEMUX, porém no esquema disponibilizado na prática, as chaves A e B eram conectadas nas entradas que eram responsáveis pela seleção de qual entrada sairia no MUX e ao mesmo tempo em qual por qual porta sairia no DEMUX, tendo assim um endereçamento fixo para cada entrada no MUX. Mas, para mudar isso, bastava conectar qualquer outras duas chaves em um dos C.I’s que teremos um controle independente para cada equipamento, podendo assim selecionar a porta que passaria pro output do MUX e também qualquer saída do DEMUX. 

Montei o circuito como pedido no roteiro, nas entradas do MUX conectei os mesmas frequências utilizadas na questão 2. Construí a tabela verdade de 4 combinações já que as mesmas chaves de seleção estavam conectadas no 2 circuitos.

Tabela verdade
A  B     MUX    DEMUX
0  0    0.1HZ  porta 9 
0  1     1HZ   port 10
1  0     10HZ  port 11
1  1     1KHZ  port 12
