# Arquitetura de Computadores - Ficha 1

## Informação do aluno

    Nome: Hélio Tavares

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Identifica e descreve os principais componentes de um processador. Fornece uma breve explicação da função de cada componente

- Lista os componentes principais de um processador.
- Para cada componente, descreve o seu papel e função no processador.
- Considera componentes como unidade lógica aritmética (ALU), unidade de controlo (UC), registos internos, memória e interfaces de entrada/saída (I/O).

P1 - Resposta:

    Unidade de controle: A unidade de controle gerencia o processamento de instruções e coordena o fluxo de dados dentro da CPU e entre outros componentes do computador. Ela tem um componente decodificador de instruções que interpreta as instruções obtidas da memória e as converte em micro-operações que a CPU pode executar. A unidade de controle direciona outros componentes da CPU para executar as operações necessárias.
    
    Unidade Lógica e Aritmética (ULA):
    Função: Realiza operações lógicas (como AND, OR, NOT) e aritméticas (como adição, subtração, multiplicação) em dados. É responsável pelos cálculos fundamentais.
    
    Registradores:
    Função: Armazenam dados temporariamente para operações rápidas. Os registradores são os locais onde a CPU realiza a maior parte de suas operações.
    
    Unidade de Ponto Flutuante (FPU):
    Função: Responsável por operações matemáticas que envolvem números de ponto flutuante, comumente usados em cálculos científicos e gráficos.
    
    Unidade de Gerenciamento de Memória (UGM):
    Função: Gerencia a leitura e escrita de dados na memória RAM. Controla o fluxo de dados entre a CPU e a memória.



### P2. Compara as arquiteturas de Von Neumann e Harvard em termos de características e principais diferenças

- Lista as principais características da arquitetura Von Neumann.
- Lista as principais características da arquitetura de Harvard.
- Explica as principais diferenças entre as duas arquiteturas, particularmente na organização da memória, busca de instruções e separação de dados.
- Fornece exemplos de sistemas de computação que usam cada arquitetura.

P2 - Resposta:

    As arquiteturas de Von Neumann e Harvard são dois modelos fundamentais de arquiteturas de computadores, e suas principais diferenças estão na maneira como tratam e armazenam dados e instruções. 
    Arquitetura de Von Neumann Compartilhado: A memória é compartilhada para dados e instruções. Ambos são armazenados no mesmo espaço de memória.
    Barramentos de Dados e Endereço:
    Único barramento: Usa um barramento único para transferir dados e endereços. Isso significa que não pode buscar instruções e dados ao mesmo tempo.
    Controle de Acesso à Memória:
    Sério: O acesso à memória é sequencial e controlado por um único barramento de controle.
    Complexidade:
    Menor complexidade: Geralmente, sistemas baseados em Von Neumann são mais simples de implementar.


    Arquitetura de Harvard:
    Armazenamento de Dados e Instruções:
    Separado: Possui memórias distintas para dados e instruções. Isso permite a busca e acesso simultâneos a dados e instruções.
    Barramentos de Dados e Endereço:
    Separado: Usa barramentos distintos para transferir dados e endereços. Isso possibilita operações paralelas de leitura/escrita de dados e instruções.
    Controle de Acesso à Memória:
    Paralelo: Permite o acesso simultâneo a dados e instruções, o que pode melhorar o desempenho em certos casos.
    Complexidade:
    Maior complexidade: A separação de memória para dados e instruções pode adicionar complexidade ao projeto.

    ...

### P3. Descreve o ciclo *fetch-decode-execute* num processador, detalhando cada etapa e explicando a sua importância na execução de programas de computador

- Fornece uma explicação detalhada da fase de busca de instrução, incluindo o que ela envolve e por que é importante na operação do processador.
- Explica a fase de descodificação e o seu papel na interpretação das instruções de execução.
- Descreve a fase de execução, destacando a execução propriamente dita das instruções e quaisquer interações com dados.
- Conclui explicando a ordem destas fases e como elas garantem a execução adequada dos programas de computador.
- Usa um diagrama para ilustrar o ciclo.

P3 - Resposta:

    O ciclo fetch-decode-execute é uma sequência de etapas que um processador realiza para executar uma instrução de um programa armazenado em memória. Essa sequência é fundamental para o funcionamento de um processador e é repetida continuamente enquanto o programa está em execução.
    
    Fetch (Buscar):
    Descrição: O processador busca a próxima instrução na memória principal (RAM) utilizando o endereço contido no registrador de instrução (PC - Program Counter).
    Importância: Essa etapa é crucial, pois obtém a próxima instrução a ser executada. O PC é incrementado para apontar para a próxima instrução após a atual.
    Decode (Decodificar):
    Descrição: A instrução recém-obtida é decodificada para que o processador entenda qual operação deve ser realizada.
    Importância: A decodificação é vital para determinar a operação específica que a instrução exige e os operandos envolvidos. Isso prepara o processador para a próxima fase.
    Execute (Executar):
    Descrição: A operação indicada pela instrução é executada utilizando a unidade de execução do processador.
    Importância: Esta é a fase onde a ação real é realizada. Pode envolver cálculos matemáticos, manipulação de dados ou controle de fluxo do programa. O resultado pode ser armazenado em registradores ou na memória.
    Write Back (Escrever de Volta):
    Descrição: Se a instrução gerou um resultado que precisa ser armazenado, este é escrito de volta na memória ou em registradores específicos.
    Importância: A etapa de write back completa o ciclo e prepara o processador para buscar a próxima instrução. O estado do processador é atualizado conforme necessário.

    Importância do Ciclo Fetch-Decode-Execute:
    Sequencialidade: O ciclo garante a execução ordenada e sequencial das instruções do programa, permitindo que as operações sejam realizadas na ordem correta.
    Controle de Fluxo: A execução sequencial das instruções permite o controle de fluxo do programa, garantindo que as decisões condicionais e os desvios sejam tratados corretamente.
    Economia de Recursos: A repetição eficiente do ciclo permite a reutilização dos recursos do processador para executar uma ampla variedade de instruções de maneira contínua.
    Automatização: A automação do ciclo permite que programas complexos sejam executados sem intervenção manual, proporcionando eficiência e praticidade na execução de tarefas computacionais.

![](https://hardzone.es/app/uploads-hardzone.es/2020/06/CPU.jpg)
