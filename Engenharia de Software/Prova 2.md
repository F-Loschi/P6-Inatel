## Métodos Ágeis
- Produtos de software são mais complexos do que outros produtos, o que faz com que o modo de produção precise ser diferente
### Waterfall
- Modelo antigo e industrial
- Montar tudo e testar e documentar apenas no final
- Não serve para software
### Manifesto Ágil
- Primeiro princípio: Software funcionando é mais importante que documentação abrangente
	- Documentação é uma funcionalidade
- Segundo princípio: Indivíduos e interações são mais importantes que processos e ferramentas
- Terceiro princípio: Colaboração com o cliente é mais importante que negociação de contratos. Solução: Contrato de benefício mútuo
- Quarto princípio: Adaptação a mudanças é mais importante que seguir um plano
- Adoção de ciclos curtos e iterativos de desenvolvimento
- Implantação ocorre gradativamente
- Começa com o "pra ontem", cliente valida e inicia novo ciclo
- A cada iteração, gera-se um incremento no sistema que pode ser validado e testado pelos usuários finais
- Ágil = Iterativo
### User Story 
 No desenvolvimento ágil, a documentação de requisitos é feita por histórias de usuários
 Documentações tradicionais sofre de:
 - Requisitos mudam
 - Linguagem natural é ambígua e incompleta
 - Sem conversas intermediárias, risco do projeto aumenta
 História de Usuário = Cartão + Conversas + Confirmação
 - Cartão: Clientes escrevem em poucas sentenças o que esperam ver
 - Conversas: Clientes explicam e detalham o que escreveram
 - Confirmação: teste de alto nível. Feito pelo cliente para verificar se foi implementado conforme esperado
 - Independentes
 - Abertas a negociação
 - Agregam valor
 - Sucintas
 - Testáveis
### Story points
- Usado para comparar tamanho de histórias
- Velocidade de um time é dado pelo quanto conseguem implementar em um sprint
### Caso de Uso
- Documentos textuais de especificação de requisitos
- Descrições mais detalhadas do que histórias de usuário
- Perspectiva de um ator que deseja usar o sistema com um objetivo
- Linguagem simples e direta
- Devem ser pequenos e com poucos passos
- Sem código ou pseudo-código
- Não deve tratar de aspectos tecnológicos ou design
- Evitar coisas muito simples
### Caso de Uso vs. Histórias de Usuário
- Caso de Uso são mais detalhados e completos
- Histórias são lembretes para facilitar o planejamento de iterações e servir para guiar conversas sobre as necessidade
- Caso de Uso documentam um acordo entre cliente e devs
## Métodos Ágeis
### XP:
- Extreme Programming
- XP = Valores + Princípios + Práticas
- Valores:
	- Comunicação:
		- Não existe bom projeto sem boa comunicação
	- Simplicidade:
		- Não se preocupar de mais com o amanhã e focar no hoje
	- Feedback
		- Algo imediato. Respostas do time de testes para time de código. Cliente pede algo e o time já estima imediatamente.
	- Coragem:
		- Para jogar fora um código, pois pensaram em uma maneira melhor de fazer
		- TDD
	- Respeito
	- Qualidade de Vida
- Princípios:
	- Economicidade:
		- Software não é uma obra de arte, mas algo que tem que gerar resultados econômicos
	- Melhorias Contínuas:
		- Mais seguro trabalhar com o continuamente aprimorado a cada iteração
	- Falhas Acontecem
		- Não devem ser acobertadas
	- Baby Steps:
		- Melhoras contínuas
	- Responsabilidade Pessoal
		- Quem implementa deve testar e manter
- Contratos:
	- Escopo Fechado:
		- Cliente define requisitos
		- Empresa desenvolvedora: preço + prazo
	- Escopo aberto:
		- Escopo definido por iteração
		- Pagamento por homem/hora
		- Renovado por iteração
		- Maturidade e acompanhamento do cliente
		- Vantagens:
			- Privilegia qualidade
			- Não vai ser enganado
Leva ao extremo tudo que é considerado bom:
- Revisar
- Teste
- Design
- Integração
- Iterações curtas
### Scrum
- Não é apenas para software
- Processo mais rígido que XP
- Desenvolvimento dividido em iterações
- A cada sprint implementa-se algumas user stories(Funcionalidades)
- Product Owner:
	- Especialista no domínio do sistema
	- Intermediário entre cliente e devs
	- PO explica histórias para devs
	- Conversas são extremamente importantes
	- Deve:
		- Escrever histórias de usuários
		- Explicar histórias para os devs durante o sprint
		- Definir teste de aceitação de histórias
		- Priorizar histórias
		- Manter o backlog
- Backlog:
	- Lista de histórias do usuário que foram escritas pelo PO
- Em uma equipe de scrum, todos têm o mesmo nível hierparquico
- PO não é "chefe" dos devs
- Scrum Board:
	- Backlog
	- To Do
	- Doing
	- Testing
	- Done
### Kanban
- Manufatura Lean
	- Foco na redução de desperdícios
- Produção Junt-in Time
	- Busca precisão da cadeia de produção
	- Operações de acordo com a demanda
- Kanban vs. Scrum:
	- Kanban é mais simples
	-  Não exitem sprints
	- Time define os papéis e eventos
- Técnica de controle visual para o balanceamento da produção
- Produz quantidade certa, no momento certo, aquilo que é necessário
- Quadro Kanban:
	- To Do
	- In Progress
	- Done

---
---
## Engenharia de Requisitos
- Requisitos definem o que um sistema deve fazer(*Requisitos Funcionais*) e sob quais restrições(*Requisitos Não-Funcionais*).
### Funcionais:
- O que o sistema fará.
- Exemplo a Netflix:
	- Play no vídeo
	- Configurar idioma
	- Gerenciar volume
	- Pausar vídeo
### Não Funcionais:
- Como o sistema fará
- No exemplo:
	- Desempenho
	- Espaço
	- Confiabilidade
	- Robustez
	- Usabilidade
### Uso de métricas
- Ajuda a não ter coisas genéricas
- "Deve ter 99,99% de disponibilidade e que 99% de todas as transações realizadas em qualquer janela de 5 minutos..."
## Tipos de requisitos:
### Requisitos de Usuário:
- Mais alto nível
- Escrito por usuário, normalmente em linguagem normal
- ***Sem detalhes técnicos***
### Requisitos de sistema
- Técnicos
- Escritos pelos devs/testers
- Requisitos Funcionais e Não-Funcionais
## Elicitação de Requisitos
- Descoberta e entendimento dos requisitos
- Falar com os clientes
- Aplicação de questionários
- Etc.
## Após a descoberta
1. Documentar:
	- No nosso caso usamos os User Stories
	- Os requisitos devem ser:
		1. Corretos
		2. Precisos
		3. Completos
		4. Consistentes
		5. Verificáveis
2. Verificar e Validar
3. Priorizar
---
- Requisitos são a "ponte" entre problema e solução de software
- Não sabemos ao certo se o nosso problema realmente é um problema, e daí surge o MVP(Minimum Viavel Product/Produto Mínimo Viável), um sistema funcional que possui apenas o conjunto mínimo de funcionalidades
	- Interessante para eliminar requisitos que não são necessários
	- Testa a viabilidade
	- Testa uma hipótese de negócio
- Métricas de vaidade: Muito acesso e pouca compra
- Métricas acionáveis: Acesso que finalizaram a compra
- --
---
## Refactoring
- Modificar o produto: facilitar o entendimento e/ou evoluir o produto de software
- Manutenção corretiva: para corrigir bug
- Manutenção evolutiva: adicionar feature nova
- Manutenção adaptativa: muda uma regra de negócio ou tecnologia
- Manutenção preventiva: bugs não aparentes
- Refactoring: Melhorias no código ou design
### Refactoring
- Transformações no código que melhoram a manutenibilidade de um sistema sem afetar seu funcionamento externo
- Catálogo:
	- Extração de Métodos:
		- Ideia geral: fazer com que um método faça apenas uma coisa e chame outro caso necessite fazer alguma outra coisa
		- Ajuda diminuir o acoplamento e manutenção de código
		- Extrair um método para ser ***reusado*** em outras partes do código
	- Inline de Métodos:
		- Sentido contrário de uma extração de método
		- Método que proporciona pouco benefício e pode ser removido
	- Movimentação de Métodos
		- Usado para refatorar métodos implementados na classe errada
		- Push up: Duas classes filhas possuem um mesmo método. Esse método pode ser jogado na classe mãe
		- Push down: Uma classe mãe tem um método que apenas uma classe filha usa. Esse método pode ser jogado na classe filha que usa.
	- Extração de Classes
		- Extrair de uma classe algo que poderia ser uma classe por si só
	- Renomeação
		- Elementos podem mudar com o tempo e a escolha de nome pode não ter sido boa, etc.
		- Problema é atualizar os pontos do código que referenciam essa classe. Normalmente faz com que o método antigo chame o novo método, mantendo seu nome, e usa-se a anotation @deprecated
- Refactoring oportunistas: 
	- Realizados no meio de uma tarefa de desenvolvimento
	- Achou algo que pode ser melhorado
- Refactoring planejado:
	- Mudanças mais profundas e planejadas
	- Devem ser raros, pois normalmente indicam que algo deu bosta
