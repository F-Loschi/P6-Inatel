## IPv4 vs. IPv6:
- IPv4 possui 32 bits no total. Possui 4 octetos de bits.
	- Um IPv4 para ser válido só pode ir até 255 em cada um de seus blocos
- IPv6 foi criado para lidar com o problema do esgotamento de endereços do IPv4. Ele possui 128 bits e usa a base hexadecimal ao invés da binária para seu endereçamento. Sua estrutura é formada por 8 grupos de 4 dígitos hexadecimais cada e separadas por :.
	- Um IPv6 para ser válido só pode ir até **F em cada um de seus dígitos hexadecimais** e, portanto, até **FFFF em cada um de seus 8 blocos**
## Máscara de sub-rede e notação CIDR:
- Usa uma '/' seguida de um número como notação
- Indica quantos bits(da esquerda para direita) estão reservados para a parte da rede, ou seja, quanto bits, da esquerda para direita, estão ligados
- Para saber quantos hosts válidos há, fazemos:
	- $$ n = 32 - X $$
	- Sendo X o valor da máscara de rede
- Com o resultado, fazemos:
	- $$ 2^n - 2 $$
	- Sendo n o valor obtido na operação anterior e '-2' pois um endereço é reservado para Rede e outro para Broadcast
- Para fazer cálculo de decimal para binário, basta pensar no octeto, quais bits estão em 1 e fazer a soma dos respectivos valores em decimal
## Endereços IP Públicos vs. Privados
- Endereços IP são divididos em 2 categorias, públicos e privados
- Públicos são usados na internet e devem ser únicos globalmente
- Privados são reservados para uso dentro de Redes Locais(LANs) e não são roteáveis na internet pública
- O IANA define algumas faixas de endereço para IPs privados:

| Classe | Bloco Inicial | Bloco Final     | Notação CIDR |
| ------ | ------------- | --------------- | ------------ |
| **A**  | 10.0.0.0      | 10.255.255.255  | /8           |
| **B**  | 172.16.0.0    | 172.31.255.255  | /12          |
| **C**  | 192.168.0.0   | 192.168.255.255 | /16          |
##  Endereçamento Dinâmico e DHCP
- O DHCP é o protocolo padrão que automatiza o processo de configuração de rede para hosts
## Modelo de Referência
### Modelo OSI
- Modelo de referência conceitual mais completo, dividido em 7 camadas
	1. Aplicação
		- Interface com o usuário
	2. Apresentação
		- Tradutor da rede
		- Garante que os dados sejam formatados de forma que a camada de aplicação entendam
		- Lida com
			- Sintaxe de dados
			- Compressão
			- Criptografia
	3. Sessão
		- Gerenciamento da comunicação entre hosts
	4. Transporte
		- Responsável pela comunicação fim-a-fim(entre o processo de uma aplicação e o processo de outra aplicação) e pela confiabilidade(como no TCP)
	5. Rede
		- Responsável por mover os pacotes através de diferentes redes(chamado de roteamento), utilizando endereços IP
	6. Enlace
		- Lida com o endereçamento físico e a comunicação dentro de uma rede local
		> Endereço MAC: Identifica o dispositivo na camada de enlace e possui 48 bits

	7. Física
		- Camada mais baixa e básica, sua única responsabilidade é lidar com a transmissão de bits brutos através do meio físico
### TCP/IP
- Modelo prático que a internet usa, mais condensado que o OSI
- Equivalência:

| Modelo OSI (7 Camadas) | Modelo TCP/IP (4 Camadas) |
| ---------------------- | ------------------------- |
| **7. Aplicação**       | **4. Aplicação**          |
| **6. Apresentação**    | **4. Aplicação**          |
| **5. Sessão**          | **4. Aplicação**          |
| **4. Transporte**      | **3. Transporte**         |
| **3. Rede**            | **2. Internet**           |
| **2. Enlace**          | **1. Acesso à Rede**      |
| **1. Física**          | **1. Acesso à Rede**      |
- Principal protocolo da camada 3 do Modelo OSI, fornece o endereçamento lógico e o roteamento de pacotes através de redes interconectadas

## Protocolos TCP, UDP e Aplicação
- Atuam na camada de transporte
### TCP
- Protocolo orientado à conexão e confiável
- Retransmite pacotes perdidos
- Mais lento
- Por ser orientado a conexão, precisa primeiro estabelecer a conexão(Handshake de três vias)
### UDP
- Mais rápido
- Baixo overhead
- Sem conexão
- Não gasta tempo verificando a ordem dos pacotes ou retransmitindo perdas. Se um pacote se perde, é melhor que o stream continue rapidamente do que esperar a retransmissão de um pacote antigo
### Porta
- O campo que garante que os dados cheguem ao **serviço/aplicativo correto** dentro do host.
- Possui 16 bits de identificação
- Uma socket é definido pela combinação do Endereço IP e Identificador de porta
### DNS
- Responsável por traduzir nomes de domínio para endereços IP