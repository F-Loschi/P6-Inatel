- Usar padrões ajuda em:
	- Continuar fazendo certo o que está dando certo
	- Documentação
- Foco em abstrair a complexidade; o que ela espera receber, o que ela faz de forma abstrata e o que ela deve devolver
- Usar padrões permite interagir e tirar proveito de entidades sem precisar dominar todos os detalhes envolvidos
- Abstrair: definir o que vai fazer sem entrar em grandes detalhes
## Propriedades
### Integridade Conceitual:
- Devemos manter uma integridade conceitual
- Integridade conceitual é sobre se manter rígido ao conceito, não ser corrompido
- O conceito se mantém firme, independente do redor
- Mantém o sistema coerente e facilita o uso para os usuários
- Não manter a integridade conceitual dificulta o uso da aplicação
### Ocultamento de Informações:
- Ocultar informações permite que classes do mesmo sistema sejam desenvolvidas mais facilmente
- Facilita mudanças quando as informações estão ocultas
- Mostrar o que é público e pradronizado e ocultar o que é privado
### Coesão
- Toda classe deve implementar uma única funcionalidade ou serviço. Todos os métodos e membros de uma classe devem atuar para implementar essa funcionalidade
	- Exemplo: um método deve calcular apenas o seno ou o cosseno, eu não devo ter uma classe que calcula os dois ao mesmo tempo 
### Acoplamento:
- Tornar as classes de forma mais desacoplada, de forma que uma classe consiga funcionar sem a existência de outra
- Quanto mais independente, melhor
- Não ter uma corrente, mas um plug
