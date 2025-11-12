## Projeto - Jogo da Velha (Java Swing)

Este projeto implementa o clássico **Jogo da Velha (Tic-Tac-Toe)** utilizando a biblioteca **Java Swing**. O foco é criar uma interface gráfica funcional onde dois jogadores podem se revezar, com a aplicação verificando automaticamente as condições de vitória e empate.

### 🚀 Sobre o Projeto

O aplicativo `JogoDaVelha` exibe um tabuleiro $3 \times 3$ composto por nove botões. O jogo alterna automaticamente o turno entre os jogadores **X** e **O** a cada clique. A interface fornece feedback visual através de um rótulo de *status* que indica de quem é a vez, ou o resultado final da partida (vitória ou empate).

### 🛠️ Tecnologias e Conceitos Abordados

**Java Swing e GUI:**
Criação da janela principal estendendo (JFrame).

**Layouts:**
Uso do `(BorderLayout)` para posicionar o *Status Label* (Norte) e o Painel do Tabuleiro (Centro).
Uso do `(GridLayout)` para organizar o painel do tabuleiro em uma grade $3 \times 3$.

**Componentes Interativos:**
Utilização de um array bidimensional de botões (`botoes[3][3]`) para representar o tabuleiro. Cada botão é o componente central da interação do jogo.

**Gerenciamento de Eventos:**
Implementação da interface `(ActionListener)` para capturar os cliques nos botões. O método `actionPerformed` gerencia o fluxo do jogo: marca o botão, inverte o turno, e verifica o estado.

**Lógica de Jogo:**

* **Controle de Turno:** A variável booleana `turnoX` rastreia de quem é a vez.
* **Verificação de Vitória:** O método `verificarVencedor()` verifica todas as 8 combinações de vitória (3 linhas, 3 colunas e 2 diagonais).
* **Verificação de Empate:** O método `verificarEmpate()` verifica se todos os botões foram preenchidos sem que houvesse um vencedor.
* **Finalização:** O método `desabilitarBotoes()` é chamado para travar o tabuleiro assim que a partida termina.

**Event Dispatch Thread (EDT):**
O método `main` garante que a aplicação seja iniciada corretamente na thread de eventos do Swing (`SwingUtilities.invokeLater`), conforme a melhor prática Java.

### 💻 Como Executar

Clone este repositório.

Este projeto deve ser compilado e executado através de um ambiente de desenvolvimento Java (IDE), como Eclipse ou IntelliJ, ou via terminal.
