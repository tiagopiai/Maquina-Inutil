# Maquina-Inutil/Useless Machine
Desenvolvimento de uma maquina inutil com o objetivo de introduzir iniciantes ao campo da robotica.

PS: O arquivo tutorial01.pdf e um guia para que o interessado busque conhecer um pouco a fundo sobre os elementos utilizados na execução
deste projeto.

As funcoes aqui implementadas tem a finalidade de simplificar o estudo daqueles que buscam uma introducao a robotica porem possuem pouca
ou nenhuma base de programacao. Assim que um conhecimento consideravel sobre programacao for desenvolvido ficara claro que tais funcoes 
nao exprimem a melhor eficiencia dos componentes utilizados e existem metodos melhores, porem relativamente mais complexos, de se 
implementar a Maquina Inutil em questao.

Funcoes

Funcao:    init_all()
Descricao: Inicializa e configura os pinos que serao utilizados para a chave e para o acionamento do Servo. Deve ser inclusa dentro do 
arquivo main.ino na funcao void setup().

Funcao:    esperaSegundos("insira o tempo em segundos aqui")
Descricao: Esta funcao faz com que o programa pare por pTempo segundos, sendo pTempo um numero real positivo.

Funcao:    checaChave("insira se deseja esperar que a chave fique ON ou OFF")
Descricao: Espera por tempo indeterminado ate que a chave seja acionada de modo ON ou OFF de acordo com o valor em pS.

Funcao:    statusChave()
Descricao: Retorna a posicao da chave ON ou OFF. Pode ser chamada dentro de um if para dizer se a chave esta ligada ou desligada.

Funcao:    acionaMotor("insira a velocidade(1 a 5)", "insira a posicao em graus que deseja que o motor esteja(0 a 180)")
Descricao: Aciona o servo motor a uma velocidade pVelocidade ate atingir a posicao pNewPos. pVelocidade pode assumir valores de 1 a 5, 
sendo 5 a velocidade máxima.

Todas essas funcoes podem ser vistas sendo aplicada no arquivo main.ino para exemplificar seu uso. Neste arquivo e possivel ver a 
presenca de dois modos bloqueante e nao bloqueante. Descomente um dos dois para ve-lo funcionando. 

O modo bloqueante requer que sejam executadas as funcoes naquela ordem especifica, ou seja, nada vai acontecer enquanto a chave nao for 
alterada. O modo nao bloqueante ja permite que outras funcoes sejam executadas enquanto a chave nao for ativada.

Pinos
Pino 9  -------------------- Sinal para o servomotor
Pino 11 -------------------- Entrada de sinal da chave

Conexoes
  Servomotor
  Fio vermelho -------------------- +5V
  Fio marrom   -------------------- GND
  Fio amarelo  -------------------- Pino 9
  
  Chave
  Pino central -------------------- GND
  Pino lateral* ------------------- Pino 11
*escolha qualquer um dos pinos laterais teste e se atente na hora da montagem. 

Construcao Mecanica
Para construcao mecanica da maquina inutil recomenda-se buscar inspiracoes em outras caixas na internet e personaliza-la de acordo com 
o seu gosto.

A biblioteca Servo.h foi obtida atraves do website: https://www.arduino.cc/en/reference/servo
