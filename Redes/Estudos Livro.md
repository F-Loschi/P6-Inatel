## Resumo do Capítulo 1
### **1.1 O que é a Internet?**

A Internet é uma vasta **rede de computadores** que interconecta bilhões de dispositivos ao redor do mundo. Esses equipamentos, chamados de **sistemas finais** ou **hospedeiros**, estão conectados por **enlaces de comunicação** (links) e **comutadores de pacotes**. A velocidade de transmissão desses enlaces é medida em bits por segundo (bps).

Quando um sistema final precisa enviar dados, ele os divide em pedaços menores, conhecidos como **pacotes**. Cada pacote recebe bytes de cabeçalho com informações de controle e é enviado através da rede. No destino, os pacotes são remontados para reconstituir os dados originais. Os comutadores, como **roteadores** e **comutadores de camada de enlace**, são responsáveis por encaminhar esses pacotes, e a sequência de enlaces e comutadores que um pacote percorre é chamada de **rota** ou **caminho**.

Para se conectar à Internet, os sistemas finais utilizam **Provedores de Serviços de Internet** (ISPs). O envio e recebimento de informações são controlados por **protocolos**, como o **TCP** (Transmission Control Protocol) e o **IP** (Internet Protocol). O IP, por exemplo, especifica o formato dos pacotes que são trocados na rede. Esses protocolos, assim como o HTTP e o SMTP, são padronizados para garantir que todos os dispositivos possam se comunicar.

A Internet pode ser vista como uma **infraestrutura que fornece serviços** a aplicações, muitas delas **distribuídas** — ou seja, envolvendo diversos sistemas finais que trocam informações entre si. Um exemplo é a navegação web, as redes sociais e os serviços de login remoto. A **Interface de Programação de Aplicação** (API) define as regras que um programa deve seguir para solicitar à infraestrutura da Internet o envio de dados a um programa de destino.

#### **1.1.3 O que é um protocolo?**
![[Pasted image 20250901141742.png]]
Um protocolo é a base da comunicação na Internet. Ele define o **formato e a ordem das mensagens** trocadas entre entidades, além das ações que devem ser realizadas no momento do envio ou recebimento de uma mensagem. Essencialmente, os protocolos são as "regras" que permitem a comunicação entre diferentes sistemas.

### **1.2 A Periferia da Internet**

Os dispositivos conectados à Internet, como computadores, smartphones e servidores, estão localizados na **periferia da Internet** e são chamados de **sistemas finais** ou **hospedeiros**. Eles podem ser divididos em:

- **Clientes:** Dispositivos de uso pessoal, como PCs, smartphones, notebooks, etc.
    
- **Servidores:** Máquinas mais poderosas que armazenam e distribuem conteúdos, como páginas web e vídeos.
![[Pasted image 20250901142820.png]]

#### **1.2.1 Redes de Acesso**

As **redes de acesso** conectam os sistemas finais (clientes e servidores) à periferia da rede. Os principais tipos de acesso residencial de banda larga são a **Linha Digital de Assinante (DSL)** e o **acesso a cabo**.

- **Acesso DSL:** Utiliza a linha telefônica de cobre já existente para fornecer acesso à Internet, geralmente pela mesma empresa que oferece o serviço de telefonia. O modem DSL de cada cliente se comunica com um **DSLAM** (multiplexador de acesso à linha do assinante digital) na central telefônica. O acesso é considerado **assimétrico** porque as taxas de transmissão (upload) e recebimento (download) são diferentes, sendo a de download geralmente maior.
	- ![[Pasted image 20250901144528.png]]
    
- **Acesso a Cabo:** Usa a mesma infraestrutura de televisão a cabo, com uma rede conhecida como **híbrida fibra-coaxial (HFC)**. O acesso é fornecido por uma operadora de TV a cabo, e o meio de transmissão é **compartilhado** entre os usuários da mesma vizinhança, o que pode afetar a velocidade da conexão. Assim como a DSL, o acesso a cabo costuma ser assimétrico.
	- ![[Pasted image 20250901143211.png]]

Outras tecnologias de acesso incluem as **redes óticas**, que podem ser ativas (AONs) ou passivas (PONs). No caso das PONs, todos os pacotes enviados do terminal de linha ótica (OLT) são replicados para os distribuidores, de forma similar ao acesso a cabo. Além disso, o **acesso via satélite** e o antigo **acesso discado** também são usados para conectar usuários à Internet.