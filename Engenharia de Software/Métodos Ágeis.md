## O Processo de Software

- **Software** é produzido de acordo com um **processo**.
    
    - É um trabalho mais **intelectual** do que mecânico.
        
    - Define um conjunto de passos, tarefas, eventos e práticas que devem ser seguidos.
        
- É essencial ter um ordenamento (mínimo que seja) para garantir:
    
    - **Qualidade** do produto.
        
    - Empresas valorizam o processo como instrumento para **coordenar, motivar, organizar e avaliar** o trabalho da equipe.
        

---

## Método Tradicional: Waterfall (Cascata)

- **Fluxo Sequencial:** Requisitos → Design → Implementação → Verificação → Manutenção.
    
- Caracterizado por uma **documentação muito extensa** e demorada.
    
- **Problemas Frequentes** em projetos de software, que se diferem da Engenharia tradicional:
    
    - Cronogramas atrasados e custo elevado.
        
    - Documentação extensa, desatualizada (apenas o código era atualizado).
        

---

## Método Ágil

- Originado a partir do **Manifesto Ágil**.
    
- **Valores Priorizados:**
    
    - **Software em funcionamento** mais do que documentação abrangente (documentação é vista como uma funcionalidade, só o necessário).
        
    - **Indivíduos e interações** mais do que processos e ferramentas (ferramentas como controle de versões e ambientes de IC continuam sendo usadas).
        
    - **Colaboração com o cliente** mais do que negociação de contratos (contrato de benefício mútuo).
        
        - Reconhece que somos ruins para planejar a longo prazo.
            
        - A interação diminui a necessidade de planejamento de longo prazo.
            
    - **Resposta a mudanças** mais do que seguir um plano (oferece vantagens competitivas).
        
- **Características Chave:**
    
    - Menor ênfase em documentação (apenas o necessário).
        
    - Menor ênfase em planos detalhados (nem o cliente sabe exatamente o que quer, como saberão os(as) engenheiros(as)?).
        
    - Inexistência de uma fase de design estática: o **Design evolui** à medida que o sistema evolui.
        
    - Uso de **Pair Programming, testes automatizados e Integração Contínua**.
        
- **Ciclos Iterativos e Incrementais:**
    
    - Principal característica: adoção de **ciclos curtos** de desenvolvimento.
        
    - A implantação ocorre de forma gradativa.
        
    - Começa-se com o que é mais urgente.
        
    - O cliente **valida** o que foi feito.
        
    - Inicia-se um novo ciclo.
        
    - O desenvolvimento termina quando o cliente decidir que o produto é satisfatório.
        

---

## Ágil vs. Tradicional

|Característica|Tradicional (Waterfall)|Ágil|
|---|---|---|
|**Entrega de Valor**|Fica pronto (e testável) apenas no final.|Cada iteração gera um **incremento** no sistema que já pode ser **validado e testado** pelos usuários finais.|

---

## Especificação de Requisitos Simplificada

### Histórias de Usuários (User Stories)

- Método de documentação de requisitos de forma simplificada.
    
- **Fórmula:** **Cartão + Conversas + Confirmação**.
    

#### 1. Cartão

- Usado pelos clientes para escrever, em sua linguagem e em poucas sentenças, uma funcionalidade esperada.
    
- Serve como um **lembrete** do requisito para os desenvolvedores.
    
- **Estrutura Comum:** "Como **[Quem]**, eu quero **[O quê]**, para **[Por quê]**."
    

#### 2. Conversas

- Interações essenciais entre clientes e desenvolvedores.
    
- Clientes **explicam e detalham** o que escreveram no cartão.
    
- A **comunicação verbal** é priorizada, pois explicações textuais não são suficientes.
    
- Espera-se que o requisito seja implementado na próxima iteração, e os clientes ficam disponíveis para a conversa.
    

#### 3. Confirmação

- Um **teste de alto nível** (Teste de Aceitação de Histórias).
    
- Feito pelo cliente para verificar se a história foi implementada conforme esperado.
    
- **Não é um teste automatizado**.
    
- As histórias são consideradas implementadas quando satisfazem os testes de confirmação.
    

### Caso de Uso

- Documentos textuais para especificação de requisitos.
    
- Incluem **descrições mais detalhadas** do que Histórias de Usuário.
    
- Geralmente escritos na fase de Especificação de Requisitos.
    
- Escritos na perspectiva de um **ator** que deseja usar o sistema com um objetivo.