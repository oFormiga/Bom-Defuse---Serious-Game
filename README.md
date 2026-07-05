# 💣 Bomb Defuse - Serious Game

Projeto desenvolvido utilizando Arduino e o Multi Function Shield, cujo objetivo é desarmar uma bomba digitando corretamente uma sequência aleatória de botões antes que o tempo acabe.

## 📖 Descrição

O jogo gera uma senha aleatória composta por 8 botões. O jogador deve reproduzir essa sequência corretamente antes que o cronômetro chegue a zero.

O tempo inicial pode ser ajustado entre **10 e 90 segundos** através do potenciômetro presente no Multi Function Shield.

Durante a partida, LEDs indicam o progresso do jogador, enquanto o buzzer fornece feedback sonoro para acertos, erros e situação crítica de tempo.

Caso toda a sequência seja digitada corretamente, a bomba é desarmada. Se o tempo acabar, ocorre o Game Over.

---

## ⚙️ Funcionalidades

- Geração aleatória de senha.
- Ajuste do tempo inicial pelo potenciômetro.
- Contagem regressiva em tempo real.
- Exibição do tempo restante no display de 4 dígitos.
- Feedback sonoro utilizando o buzzer.
- Indicação do progresso através dos LEDs em binário.
- Aumento da velocidade da contagem regressiva após erros.
- Exibição da senha no Monitor Serial ao final da partida.

---

## 🎮 Como jogar

1. Ajuste o tempo utilizando o potenciômetro.
2. Pressione qualquer botão para iniciar.
3. O display exibirá **GO**.
4. Digite corretamente a sequência gerada.
5. Cada acerto acende os LEDs indicando o progresso.
6. Um erro reinicia a sequência e aumenta a velocidade da contagem.
7. Complete os 8 acertos antes que o tempo termine.

---

## 🔌 Hardware utilizado

- Arduino Uno
- Multi Function Shield
- Display de 4 dígitos
- Potenciômetro
- 3 Botões
- 4 LEDs
- Buzzer

---

## 📥 Entradas

| Entrada | Tipo | Função |
|----------|------|--------|
| Potenciômetro | Analógica | Ajusta o tempo inicial (10 a 90 segundos). |
| Botões | Digital | Iniciam o jogo e inserem a sequência da senha. |

---

## 📤 Saídas

| Saída | Função |
|--------|---------|
| Display | Exibe tempo restante e mensagens ("GO", "OFF"). |
| LEDs | Indicam o progresso da sequência em binário. |
| Buzzer | Sons de início, acerto, erro, tempo crítico e fim do jogo. |
| Monitor Serial | Exibe mensagens de status e revela a senha ao final da partida. |

---

## 📋 Lógica do jogo

1. Ler o potenciômetro.
2. Definir o tempo inicial.
3. Gerar uma senha aleatória de 8 posições.
4. Esperar o jogador iniciar a partida.
5. Iniciar a contagem regressiva.
6. Comparar cada botão pressionado com a senha.
7. Se acertar:
   - Avança para o próximo índice.
   - Atualiza os LEDs.
8. Se errar:
   - Reinicia a sequência.
   - Aumenta a velocidade do cronômetro.
9. Se completar toda a sequência:
   - Exibe "OFF".
   - Finaliza o jogo com sucesso.
10. Se o tempo acabar:
    - Executa o Game Over.

---

## 📚 Bibliotecas utilizadas

- TimerOne
- MultiFuncShield

---

## 👨‍💻 Autor

Tiago Henrique Gomes Formiga

Projeto desenvolvido para a disciplina de Integração de Hardware e Software.
