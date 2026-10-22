[[Teste de Software]]
## Ferramentas  
- **JUnit**  
- **Mockito**  
  - Ambas são dependências externas amplamente utilizadas no ecossistema Java.  

## Conceitos Fundamentais  
- A **unidade** é definida pelo time de desenvolvimento.  
  - Para nosso contexto, consideraremos **classe** como unidade.  
- Um **teste** é implementado como um **método anotado com `@Test`** (JUnit).  
- Testes devem conter **assertivas** para validar resultados, como:  
  - `assertEquals`  
  - `assertTrue`  
  - `assertFalse`  
- **Suíte de Teste**: conjunto de casos de teste agrupados.  
- **SUT (System Under Test)**: o sistema ou parte dele que está sendo testado.  
  - É fundamental conhecer o sistema para definir o que deve ser testado.  

## TDD - Test Driven Development (Desenvolvimento Guiado por Testes)  
- Ideia: escrever o teste **antes** da funcionalidade existir.  
- Garante que cada funcionalidade já seja entregue com testes.  
- Vantagem: força o desenvolvedor a pensar no comportamento esperado do código.  

---

## Quando Fazer Testes  

### Modelo Cascata  
- Testes realizados apenas quando o sistema já está pronto.  
- **Problemas**:  
  - Possibilidade de encontrar erros no final do projeto.  
  - Bugs podem aparecer somente quando o cliente já estiver utilizando o sistema.  
- **Não é a abordagem ideal.**  

### Métodos Ágeis  
- Testes desenvolvidos em paralelo à implementação das funcionalidades.  
- **Benefícios**:  
  - Reduz a quantidade de bugs.  
  - É a abordagem mais usada no mercado.  

### Regressão  
- Introdução proposital de um erro em algo que já funcionava.  
- Objetivo: verificar se os testes estão realmente cobrindo aquele cenário.  

---

## Princípios FIRST  

### **F - Fast (Rápido)**  
- Deve ser executado com frequência, portanto precisa ser rápido.  

### **I - Independent (Independente)**  
- A ordem de execução não deve influenciar o resultado.  
- Os testes não podem:  
  - Alterar o estado global do sistema.  
  - Depender uns dos outros.  

### **R - Repeatable (Repetível)**  
- O resultado deve ser sempre o mesmo, seja em 1 execução ou em 1000.  
- **Concorrência** é a principal causa de resultados intermitentes.  

### **S - Self-Checking (Auto-Verificável)**  
- O teste deve indicar automaticamente se passou ou falhou.  

### **T - Timely (Oportuno)**  
- Deve ser escrito o quanto antes.  

> ⚠️ Boa prática: cada teste deve conter **apenas uma assertiva**, para facilitar a identificação do erro.  