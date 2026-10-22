[[Aula 3]] – É importante considerar tanto a Aula 3 quanto esta ao desenvolver código.  

- O software é complexo e naturalmente propenso a erros.  
- Erros podem causar desconforto, prejuízos financeiros ou até catástrofes.  
- Antigamente, os testes eram realizados de forma **manual**:  
  - Processo entediante, repetitivo e sujeito a falhas.  
  - Muitas vezes delegado a estagiários.  
- Atualmente, os testes são **automatizados**:  
  - Podem ser implementados em paralelo ao desenvolvimento das funcionalidades.  
  - Se o software não for testável, ele precisa ser reestruturado.  
- Os testes não servem apenas para encontrar bugs, mas também para **garantir a qualidade e a continuidade** do sistema.  
- Além disso, podem servir como **documentação viva** do projeto.  
- A maior parte dos testes deve ser **unitária**:  
  - Quanto maior a cobertura de testes unitários, menor a necessidade de testes de integração.  
  - Consequentemente, isso reduz também a quantidade de testes de sistema.  

---

## Tipos de Teste  
- **Teste de Unidade**: avalia uma única parte isolada do sistema.  
- **Teste de Integração**: verifica a comunicação entre partes do sistema.  
- **Teste de Sistema**: valida o funcionamento do software como um todo.  

---

## Teste Unitário  

- São testes automatizados que verificam pequenas unidades de código de forma isolada.  
- **Unidade**: geralmente uma **classe**, mas pode ser outro elemento mínimo do sistema.  
- Objetivo: garantir que os métodos retornem os resultados esperados.  
- Estrutura:  
  - **Classes de requisitos** (implementação do sistema).  
  - **Classes de teste** (validação do comportamento).  
- **Teste com Mock**:  
  - Ferramenta que simula o comportamento de dependências externas de forma controlada.  
  - Exemplo: quando os dados necessários estão em um servidor remoto ainda não disponível, mas o formato do JSON já é conhecido.  

---

## Teste de Integração  

- O objetivo é validar o funcionamento conjunto de várias classes ou módulos do software, garantindo que a **funcionalidade completa** opere corretamente.  
- Não existe uma regra fixa sobre quantas classes devem ser integradas para caracterizar esse tipo de teste.  
- Diferença essencial: ao contrário dos testes unitários, não se deve usar **Mock**, mas sim o sistema real.  
- Alguns desenvolvedores consideram que só há teste de integração quando as classes testadas pertencem a pacotes diferentes.  