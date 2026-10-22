[[Aula 2]]
Um *SCV* (*Sistema de **Controle de **V*ersões) é um repositório que armazena projetos com versionamento do projeto, a utilização disso é para a possível necessidade de recuperar uma versão anterior do projeto.

São sistemas centralizados e baseados na arquitetura cliente/servidor 

 ![[Pasted image 20250811205744.png]]
 
 O problema desse método é que ele é centralizado em somente em um servidor, portanto se houver um problema com o servidor ou o projeto, praticamente acabou com o projeto.

![[Pasted image 20250811210436.png]]
## Sistemas Controle de Versões Distribuídos (DVCS) 
- Cada Cliente possui um repositório local completo
- Na prática existe uma máquina principal com uma versão referente ao código fonte (Repositório Central)
- Os Clientes também podem trabalhar de forma off-line realizando commits no repositório local
### Vantagens do DVCS
- A maioria das operações são mais rápidas, pois podem ser feitas localmente.
- As operações de *commit* são realizadas com uma maior frequência

### Comandos de Sincronização:
Os comandos  push  e  pull  servem para fazer uma sincronização com o repositório remoto, onde o  push  envia todas as modificações e os commits locais, e o  pull  faz o contrario, recebendo todas as modificações e commits remotos, deixando assim o repositório local Sincronizado com a versão remota.

### Monorepos vs Multirepos 
Ambos são métodos de organização nas quais os sistemas e/ou projetos são guardados. O *Monorepos* sendo uma forma em que todos os sistemas/projetos são guardados em um único repositórios, tendo assim todos centralizados em um só local. Já os *Multirepos* é uma forma onde os sistemas/projetos são guardados em vários repositórios, sendo um repositório para cada sistemas/projetos.
![[Pasted image 20250814161003.png]]

---
# Git
Utiliza *Git* como *DVCS*.
- Armazena os dados como snapshots (fotografias instantâneas).
- Cada *commit* é como se uma "foto" fosse torada do arquivo, e uma referência a essa foto também é armazenada. 
- Gerencia o sistema como um fluxo de fotografias.
- E as snapshots são armazenadas em um formato compacto.
- A maioria das operações são *locais*.
- Podemos acessar o histórico de modificações de um arquivo localmente (esse é outro fator que o torna rápido)
- Requer conexão online apenas para sincronizar com o repositório central, ou seja pull e push.
- O Git manipula *Três Áreas*:
	1. *Diretório de Trabalho* (Working Directory): Onde se encontra os arquivos que queremos versionar.
	2. O *Repositório* propriamente dito: É um arquivo .git que armazena o histórico de commits.
	3. Uma área intermediária chamada de Stage: É nela que se armazena temporariamente os arquivos que pretendemos versionar. Esses arquivos são chamados de tracked files. 

- O desenvolvedor acessa apenas o diretório de trabalho (é um diretório comum) e este pode conter diversos arquivos.
- *Apenas* os arquivos adicionados a área Stage serão gerenciados pelo Git. O comando  add  adiciona um ou mais arquivos ao Stage.
- A área Stage também armazena o conteúdo dos arquivos (além de uma lista com o nome dos arquivos).
- *Apenas* arquivos que estão na Stage podem ser "commitados". 
![[Pasted image 20250814164956.png]] 
- *ATENÇÃO!!!* Não se deve realizar um único commit que contempla mais de uma modificação.