🚀 Desenvolvimento de sistema embarcado para identificação de componentes espectrais utilizando ATmega328P

Durante o desenvolvimento do Projeto II da disciplina de Microcontroladores I, foi desenvolvido um sistema embarcado completo para aquisição e identificação de componentes de frequência em sinais analógicos.

O projeto envolveu o desenvolvimento de uma placa dedicada, utilizando o ATmega328P com cristal externo de 16 MHz, permitindo uma temporização precisa para aquisição dos sinais e processamento embarcado.

A grande proposta do projeto foi implementar um método de identificação espectral diretamente no microcontrolador, sem depender de processamento externo. Para isso, foi desenvolvido em linguagem C o método P/Q/S (projeção ortogonal em seno e cosseno), onde o sinal adquirido pelo ADC é comparado com referências senoidais conhecidas, permitindo estimar a amplitude de frequências específicas através da magnitude resultante das componentes em fase e quadratura.

O algoritmo foi otimizado para as limitações de um microcontrolador de 8 bits, utilizando aritmética de ponto fixo, tabela seno armazenada em memória de programa e sem utilização de funções trigonométricas ou ponto flutuante durante o processamento.

O sistema realiza:
⚡ Aquisição de sinais pelo ADC de 10 bits;
⚡ Remoção dinâmica do offset DC;
⚡ Identificação de harmônicos de 60 Hz até 300 Hz;
⚡ Detecção de sinais DTMF através das frequências características;
⚡ Comunicação serial para supervisão dos dados.

Para análise dos resultados, foi desenvolvida uma interface em MATLAB, responsável pela leitura dos dados enviados pelo microcontrolador e geração do espectro harmônico, permitindo visualizar as componentes identificadas pelo algoritmo.

Na validação experimental, foram aplicados sinais de 60 Hz, 120 Hz e 300 Hz, obtendo erros inferiores a 1% entre os valores aplicados e medidos, demonstrando a eficiência da solução desenvolvida.

Esse projeto proporcionou uma integração completa entre eletrônica analógica, projeto de hardware, firmware embarcado e processamento digital de sinais, resultando em uma solução de instrumentação de baixo custo capaz de realizar análises normalmente associadas a equipamentos dedicados.

#EngenhariaElétrica #SistemasEmbarcados #Microcontroladores #ATmega328P #DSP #ProcessamentoDigitalDeSinais #EmbeddedSystems #Eletrônica
