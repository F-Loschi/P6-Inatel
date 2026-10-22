[[Aula 1]]
## Definições:
- **Dependência**: Quando eu estou fazendo um software e preciso de um outro software para fazer algo no meu
	- As bibliotecas são um exemplo de software
## Dependência:
- Posso baixa-las manualmente, mas não compensa porque as dependências podem ser atualizadas e eu teria que ir baixar a atualização
	- Fica insustentável quando se pensa em um software feito por uma equipe inteira
- Mais fácil automatizar isso colocando a instrução pro gerenciador
## Build:
- **Empacotar** o seu código com ele e todas as dependências e tudo necessário para rodá-lo
- Também chamado de **produto**
- Quando empacota o software, um arquivo Jar é criado
- É o que o usuário final usa
## Gerenciador:
- Existe mais de um tipo de gerenciador para uma mesma linguagem
	- Exemplo: Maven - Gerência as dependências e automatiza a build em Java
- MVNRepository:
	- Um repositório central onde estão armazenados as dependências gerenciadas pelo Maven
	- Ao clicar na versão da dependência que queremos, o MVNRepository te dá o texto para automatizar a build dessa dependência no Maven
	- Toda configuração do Maven é feita através do pom.xml
	- Nesse arquivo definimos tudo que precisamos que o Maven cuide para a build automatizada do nosso projeto, inclusive a gerência das dependências
		- Podemos configurar as dependências, o nome do jar, o tipo de empacotamento, o escopo das dependências, executar apenas os testes, etc
## E a Build:
- Com o comando mvn package, o Maven:
	- Compila o projeto
	- Executa os testes de unidade (que estiverem em src/main/test)
	- Gera o jar
	- O comando deve ser executado na raiz
	- Estando dentro do pom.xml no projeto e abrindo o terminal, podemos:
		- "mvn clean install" - para limpar o código e instalar as dependências necessárias
		- "mvn clean install" - para buildar