---

**Questão central:** Definir claramente que tipo de informação deve ser recebida, de que forma e quem será responsável por chamar cada funcionalidade.

---

## Tema 1

### Equipe 7 – _Cadastro de Jogadores_

**Pontos positivos:**

- Consideraram registro, verificação, comparação e alteração de dados.
- Definiram apenas login e cadastro como escopo principal.
- Preocupação com segurança de senha utilizando **hash**.

**Pontos negativos:**

- Não abordaram a relação com a distribuição de cartas (se irão chamar ou ser chamados continuamente).
- Todos os métodos foram definidos como public, o que não é adequado.
- Não houve previsão de verificação e gerenciamento de token.
- Ausência de checagem de privilégios para determinar se o usuário é administrador.    

---

## Tema 2

### Equipe 3 – _Distribuição de Cartas_

Meu grupo

---

## Tema 3

### Equipe 2 – _Trocas_

**Pontos positivos:**

- Estruturaram bem o projeto e distribuíram as responsabilidades entre os integrantes.

**Pontos negativos:**
- Inseriram elementos de Front-end e API (não condizentes com o tema).
- Focaram excessivamente em ferramentas, sem aprofundar o tema do projeto.
- Apresentação superficial dos diagramas, tornando-os confusos.

---

## Tema 4

### Equipe 8 – _Visualização de Carta_

**Pontos positivos:**

- Conexões feitas de forma correta.    

**Pontos negativos:**

- Falta de comunicação com os outros grupos gerou inconsistências na previsão de métodos.
- Idealmente, o player deveria atuar como hub para centralizar a comunicação.
- Ausência de uma classe de controle explícita (ainda que abstraída).
- Relação de agregação excessivamente forte entre classes.

---

## Tema 5

### Equipe 6 – _Visualização de Troca_

**Pontos positivos:**

- Consideraram a criação de um marketplace.
- Integração direta com a parte de visualização de cartas.
- Ideia consistente de marketplace com moeda obrigatória de carta (mantendo a regra das 5 cartas por jogador).
- Dependência clara da renderização de cartas.

**Pontos negativos:**
- Falta de integração com a autenticação, apesar de utilizarem informação do usuário logado.
- Ausência de alinhamento com o back-end, gerando incompatibilidade.
- Não definiram claramente o que receber e como receber do back.
- Casos de uso foram pensados em termos de páginas, não em termos de agentes e ações.
- Erros no uso de setas no diagrama de caso de uso.

---

## Tema 6
### Equipe 5 – _Painel de Administração_
**Pontos positivos:**
- Ligação direta com o módulo de trocas.
- Não duplicaram a base de login (responsabilidade de outro grupo).
- Uso interessante de API síncrona para consultas.

**Pontos negativos:**
- Uso incorreto de extends e include (nem todo jogador acessa todas as informações).
- Diagramas sobrecarregados, com excesso de informações.

---

## Tema 7

### Equipe 1 – _Sistema de Gestão de Batalha_
**Pontos positivos:**

- Integração com o ranking de jogadores.
- Sistema de solicitação de partida com validação de rank.
- Matchmaking associado ao sistema de filas.
- Necessidade de coleta de informações dos jogadores.
- Gestão do ranking com base nas notificações de resultados.

**Pontos negativos:**
- Não previram que a manutenção do ranking é responsabilidade do próprio grupo.
- Nomes dos métodos pouco claros.
- Ausência de ator representando o banco de dados.

---

## Tema 8

### Equipe 4 – _Batalha_

**Pontos positivos:**

- Liberdade para o jogador escolher qual carta iniciar.
- Integração com o módulo de distribuição de cartas para selecionar os Pokémon iniciais.

**Pontos negativos:**

- Explicação insuficiente sobre o uso de extends.
- Falta de conexão com o gerenciador de partidas e com as cartas dos jogadores.
- Conexão incoerente entre distribuição de cartas e jogador.

---

## Tema 9

### Equipe 9 – _Pokédex_

**Pontos positivos:**

- Relação direta com a distribuição de cartas para identificar quais cartas o jogador conhece.    
- Funções bem definidas: marcar carta como conhecida e consultar posteriormente.
- Diagrama mais organizado.
- Equipe demonstrou maior organização geral.

**Pontos negativos:**

- Não especificaram se a Pokédex exibirá apenas as cartas conhecidas ou se incluirá também as desconhecidas com “?”.
- Não planejaram relacionar jogadores com os adversários já enfrentados.

---
