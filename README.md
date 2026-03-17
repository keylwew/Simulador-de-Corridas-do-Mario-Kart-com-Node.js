# Simulador-de-Corridas-do-Mario-Kart-com-Node.js

#  Simulador de Corridas do Mario Kart - Node.js

Este projeto é um simulador de corridas inspirado no universo Mario Kart, totalmente executado no terminal usando Node.js.  
O jogador escolhe um personagem e compete contra adversários controlados pelo sistema, podendo utilizar itens clássicos para ganhar vantagem.

---

##  Objetivo

- Reproduzir a lógica de corridas de Mario Kart no backend  
- Desenvolver interação com o usuário via terminal  
- Trabalhar lógica de programação, aleatoriedade e uso estratégico de itens  
- Criar um projeto funcional para portfólio e entrega de desafio da DIO  

---

##  Regras do Jogo

1. Cada jogador escolhe um personagem com atributos de **velocidade** e **aceleração**.  
2. A corrida ocorre em múltiplos **turnos (rounds)**.  
3. Em cada turno, todos os jogadores avançam de acordo com seus atributos + fator aleatório.  
4. Itens podem ser adquiridos aleatoriamente durante a corrida.  
5. O jogador pode usar itens para afetar adversários ou a si mesmo.  
6. Ao final de todos os turnos, é exibido o **placar final** com o posicionamento dos participantes.  
7. Aquele que estiver na **primeira posição ao final** é o vencedor.  

---

##  Objetos do Jogo

- **Personagem/Jogador**: cada um tem `nome`, `velocidade`, `aceleração`, `posição` e lista de `itens`.  
- **Itens disponíveis**:
  - **Banana**: faz o adversário escorregar (-1 posição)  
  - **Casco Vermelho**: atinge adversário (-2 posições)  
  - **Estrela**: aumenta a velocidade do jogador (+2 posições)  
- **Corrida**: objeto que controla os turnos, movimentos, uso de itens e posições.  
- **Placar**: lista com a posição atual de cada jogador em cada turno.

---

##  Início do Jogo (Start)

1. O jogo inicia exibindo uma mensagem de boas-vindas.  
2. O jogador escolhe seu personagem entre os disponíveis.  
3. Os demais personagens se tornam adversários automáticos.  
4. A corrida começa com o **primeiro turno**, e todos os jogadores avançam de acordo com atributos e aleatoriedade.

---

##  Round / Turno

Em cada turno:  

1. Cada jogador avança baseado em `velocidade + aleatoriedade`  
2. Itens podem ser adquiridos aleatoriamente pelo jogador.  
3. Jogadores podem **usar itens** contra adversários ou a si mesmo.  
4. É exibido o **placar parcial**, mostrando posições e itens adquiridos.  
5. O turno seguinte começa até que todos os rounds sejam concluídos.

---

##  Uso de Itens

- **Banana**: usado contra outro jogador; adversário perde 1 posição  
- **Casco Vermelho**: usado contra outro jogador; adversário perde 2 posições  
- **Estrela**: usado pelo próprio jogador; ganha avanço extra de 2 posições  

> Estratégia: usar itens no momento certo pode mudar o placar e garantir vitória!

---

##  Game Over / Resultado Final

- Ao final de todos os rounds, o sistema calcula as posições finais.  
- É exibido o **placar final** com todos os jogadores e suas posições.  
- O jogador que terminar em **primeiro lugar** vence a corrida.  
- Mensagens de destaque são exibidas no terminal com cores para facilitar leitura.

---

##  Estrutura do Projeto
