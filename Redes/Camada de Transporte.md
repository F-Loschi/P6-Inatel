[[Fundamentos de Redes]]
# Camada de Transporte: TCP vs UDP

## O que é a Camada de Transporte?

Imagine que você quer enviar uma carta para um amigo. A camada de transporte é como o **serviço dos correios** - ela garante que sua mensagem chegue do seu computador até o computador do destinatário de forma organizada.

### Principais funções:

- **Transferência confiável**: Como um correio registrado que confirma a entrega
- **Eficiência**: Otimizar o envio sem desperdiçar recursos
- **Economia**: Usar a rede de forma inteligente

---

## Tipos de Serviços

### 🔗 Orientado a Conexão (TCP)

É como **ligar para alguém**: primeiro você disca, espera atender, fala "alô", confirma que é a pessoa certa, e só então conversa.

**Exemplo prático**: Quando você acessa seu banco online, precisa que TODOS os dados cheguem corretamente e na ordem certa.

### 📮 Não Orientado a Conexão (UDP)

É como **enviar um SMS**: você simplesmente envia e torce para chegar. Rápido, mas sem garantias.

**Exemplo prático**: Jogos online onde é melhor perder um frame do que atrasar o jogo todo.

---

## [[UDP]] - User Datagram Protocol

### 🚀 Características principais:

- **Simples e rápido**: Como enviar um telegrama
- **Sem garantias**: Pode não chegar ou chegar fora de ordem
- **Sem controles**: Não verifica congestionamento ou erros

### 📦 Estrutura do pacote UDP:

- **Porta de origem**: De onde veio (como o remetente)
- **Porta de destino**: Para onde vai (como o destinatário)
- **Comprimento**: Tamanho da mensagem
- **Checksum**: Uma "assinatura" para verificar se não foi corrompido

### 🎯 Quando usar UDP:

- **Streaming de vídeo**: Netflix, YouTube (melhor perder alguns pixels que pausar)
- **Jogos online**: Counter-Strike, Fortnite (velocidade > perfeição)
- **DNS**: Consultas rápidas de endereços de sites

---

## [[TCP]] - Transmission Control Protocol

### 🛡️ Características principais:

- **Confiável**: Garante que tudo chegue e na ordem certa
- **Orientado à conexão**: Estabelece uma "conversa" antes de enviar dados
- **Com controles**: Verifica erros, controla fluxo e congestionamento

### 📋 Estrutura do pacote TCP (mais complexa):

Além das portas, tem:

- **Número de sequência**: Para ordenar as mensagens
- **ACK**: Confirmação de recebimento
- **Janela**: Quanto o receptor pode receber
- **Flags**: Sinais especiais (SYN=iniciar, FIN=terminar)

### 🎯 Quando usar TCP:

- **Navegação web**: Sites, formulários, downloads
- **Email**: Suas mensagens devem chegar inteiras
- **Transferência de arquivos**: Downloads, uploads
- **Banco online**: Transações que não podem ter erro

---

## Principais Mecanismos do TCP

### 1. 🎪 [[Multiplexação e Demultiplexação]]

**Analogia**: Como um prédio de apartamentos com vários moradores

- **Multiplexação**: O porteiro (seu computador) recebe várias cartas e organiza todas em um saco para enviar
- **Demultiplexação**: O porteiro do destino recebe o saco e distribui cada carta para o apartamento correto

**Exemplo real**: Seu computador rodando WhatsApp, Netflix e navegador ao mesmo tempo, cada um usando uma "porta" diferente.

### 2. ✅ [[Controle de Erro e Retransmissão]]

**Analogia**: Como uma conversa por walkie-talkie

- Você fala: "Alô, você me ouve? Câmbio"
- Resposta: "Recebi! Câmbio"
- Se não receber resposta, repete a mensagem

**Exemplo real**: Quando você envia uma mensagem no WhatsApp e aparece ✓ (enviado) e ✓✓ (entregue).

### 3. 🌊 [[Controle de Fluxo]]

**Analogia**: Como encher um balde furado

- Se você despeja água muito rápido, transborda
- O TCP ajusta a velocidade conforme a capacidade do receptor

**Exemplo real**: Download que vai mais devagar quando seu HD está quase cheio.

### 4. 🚦 [[Controle de Congestionamento]]

**Analogia**: Trânsito em uma avenida

- **Trânsito livre**: Acelera e envia mais dados
- **Trânsito pesado**: Diminui a velocidade para não causar engarrafamento
- **Acidente**: Para quase completamente (partida lenta)

#### Fases do controle de congestionamento:

**🐌 [[Partida Lenta]]**

- Começa enviando poucos dados
- Dobra a velocidade a cada confirmação
- Como um carro acelerando aos poucos na entrada da rodovia

**⚠️ [[Prevenção de Congestionamento]]**

- Quando detecta que a rede está ficando cheia
- Aumenta mais devagar para não sobrecarregar
- Como reduzir velocidade ao ver trânsito à frente

**🏃 [[Recuperação Rápida]]**

- Quando perde apenas alguns pacotes (não todos)
- Diminui um pouco a velocidade, mas não para completamente
- Como mudar de faixa quando vê um problema específico

---

## 🤔 TCP vs UDP: Quando usar cada um?

### Use TCP quando:

- ✅ Precisão é fundamental
- ✅ Não pode perder informações
- ✅ Ordem importa
- **Exemplos**: Email, navegação web, downloads, banco online

### Use UDP quando:

- ⚡ Velocidade é prioridade
- 🎮 Tempo real é crucial
- 📺 Perder alguns dados não é problema
- **Exemplos**: Jogos online, streaming, videochamadas, DNS

---

## 💡 Resumo Prático

Think of it this way:

- **TCP** = Correio registrado (confiável, mas mais lento)
- **UDP** = Pombo correio (rápido, mas pode se perder)

A internet usa ambos dependendo da situação - sua experiência online é uma combinação inteligente dos dois protocolos trabalhando juntos!