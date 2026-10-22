## Definição e Propósito
- **Regras e diretrizes** para criação de software sustentável
- **Recomendações** para manter alta coesão e baixo acoplamento
- **Pensado para softwares** que serão mantidos, evoluídos e estendidos ao longo do tempo
- **Fundamentais** para desenvolvimento ágil e manutenibilidade

## Princípios SOLID

### 1. Single Responsibility Principle (SRP)
**"Cada módulo deve ter uma e apenas uma razão para mudar"**

- ✅ **Um único motivo** para modificar um componente
- ✅ **Fortalecimento da coesão** - elementos relacionados ficam juntos
- ✅ **Separação de preocupações** distintas
- ✅ **Facilita testes** e manutenção

**Como violar:**
- ❌ Acoplar responsabilidades completamente diferentes
- ❌ Classes "God objects" que fazem tudo
- ❌ Métodos com múltiplas finalidades não relacionadas

**Exemplo de violação:**
```java
// ❌ Viola SRP - múltiplas responsabilidades
class Relatorio {
    void calcularImpostos() { /* ... */ }
    void salvarParaArquivo() { /* ... */ }
    void enviarPorEmail() { /* ... */ }
    void formatarHTML() { /* ... */ }
}
```

### 2. Open/Closed Principle (OCP)
**"Aberto para extensão, fechado para modificação"**

- ✅ **Extensibilidade** sem modificar código existente
- ✅ **Prevenção** de quebras em interfaces consolidadas
- ✅ **Uso de interfaces** para encapsular comportamentos variáveis
- ✅ **Herança e composição** para adicionar novas funcionalidades

**Implementação:**
```java
// ✅ Segue OCP
interface Forma {
    double calcularArea();
}

class Circulo implements Forma { /* implementação */ }
class Retangulo implements Forma { /* implementação */ }
// Novas formas podem ser adicionadas sem modificar código existente
```

### 3. Liskov Substitution Principle (LSP)
**"Classes derivadas devem ser substituíveis por suas classes base"**

- ✅ **Uso correto do polimorfismo**
- ✅ **Consistência comportamental** nas hierarquias de herança
- ✅ **Prevenção** de surpresas desagradáveis com subtipos
- ✅ **Contracts** devem ser mantidos pelas subclasses

**Violação clássica:**
```java
// ❌ Viola LSP - Quadrado não se comporta como Retangulo
class Retangulo {
    void setLargura(double w) { /* ... */ }
    void setAltura(double h) { /* ... */ }
}

class Quadrado extends Retangulo {
    void setLado(double s) { /* ... */ }
    // setLargura e setAltura quebram o comportamento esperado
}
```

### 4. Interface Segregation Principle (ISP)
**"Prefira interfaces específicas e pequenas"**

- ✅ **Interfaces focadas** em comportamentos específicos
- ✅ **Evita** que clientes implementem métodos não utilizados
- ✅ **Separação** de concerns em interfaces distintas
- ✅ **Flexibilidade** na implementação

**Exemplo:**
```java
// ✅ Segue ISP - Interfaces segregadas
interface Imprimivel {
    void imprimir();
}

interface Digitalizavel {
    void digitalizar();
}

interface Copiadora {
    void copiar();
}

// Clientes implementam apenas o necessário
```

### 5. Dependency Inversion Principle (DIP)
**"Dependa de abstrações, não de implementações concretas"**

- ✅ **Acoplamento** com interfaces, não com implementações
- ✅ **Flexibilidade** para trocar implementações
- ✅ **Testabilidade** facilitada por mocking
- ✅ **Inversão de controle** e injeção de dependências

**Implementação:**
```java
// ✅ Segue DIP
interface BancoDeDados {
    void salvar(Dados dados);
}

class MySql implements BancoDeDados { /* ... */ }
class MongoDB implements BancoDeDados { /* ... */ }

class Servico {
    private BancoDeDados db; // Dependência da abstração
    Servico(BancoDeDados db) { this.db = db; } // Injeção
}
```

## Resumo SOLID × Propriedades de Design

| Princípio               | Propriedade Fortalecida | Benefício Principal               |
|-------------------------|-------------------------|-----------------------------------|
| Responsabilidade Única  | Coesão                  | Manutenibilidade                  |
| Segregação de Interfaces| Coesão                  | Flexibilidade de implementação    |
| Inversão de Dependências| Baixo Acoplamento       | Testabilidade e Flexibilidade     |
| Aberto/Fechado          | Extensibilidade         | Estabilidade com Evolução         |
| Substituição de Liskov  | Extensibilidade         | Consistência Polimórfica          |

## Lei de Demeter (Princípio do Menor Conhecimento)

**"Só converse com seus amigos íntimos"**

### Métodos podem invocar:
- ✅ **Própria classe** (this)
- ✅ **Objetos passados como parâmetros**
- ✅ **Objetos criados pelo próprio método**
- ✅ **Atributos da própria classe**

### Regra "um ponto" (one dot rule):
```java
// ❌ Viola Demeter - conhece muitos detalhes
cliente.getEndereco().getCidade().getNome();

// ✅ Segue Demeter - encapsula a complexidade
cliente.getCidade(); // A própria classe Client fornece o método
```

### Benefícios da Lei de Demeter:
- ✅ **Reduz acoplamento** entre classes
- ✅ **Aumenta encapsulamento** e informação hiding
- ✅ **Facilita mudanças** - menos dependências diretas
- ✅ **Melhora manutenibilidade** - menos pontos de quebra

### Exemplo de implementação:
```java
// ✅ Segue Lei de Demeter
class Pedido {
    private Cliente cliente;
    
    public String getCidadeCliente() {
        return cliente.getCidade(); // Cliente encapsula seus detalhes
    }
}

class Cliente {
    private Endereco endereco;
    
    public String getCidade() {
        return endereco.getCidade(); // Endereco encapsula seus detalhes
    }
}
```

## Benefícios Combinados dos Princípios

### Para Desenvolvimento:
- ✅ **Código mais limpo** e organizado
- ✅ **Facilidade de testes** unitários
- ✅ **Refatoração segura** e previsível

### Para Manutenção:
- ✅ **Menor impacto** nas mudanças
- ✅ **Maior compreensão** do código
- ✅ **Menor tempo** de onboarding

### Para Arquitetura:
- ✅ **Sistemas mais flexíveis** e adaptáveis
- ✅ **Melhor escalabilidade** horizontal e vertical
- ✅ **Evolução contínua** sem rupturas

## Ferramentas e Práticas Relacionadas
- **Injeção de Dependência**: Spring, Guice, Dagger
- **Testes Unitários**: JUnit, Mockito, Jest
- **Análise Estática**: SonarQube, Checkstyle, PMD
- **Refactoring**: Técnicas sistemáticas de melhoria de código

---

**[[Design Patterns]]** | **[[Clean Code]]** | **[[Arquitetura de Software]]** | **[[Testes Unitários]]** | **[[Refactoring]]**