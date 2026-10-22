## Definição Básica

- **Mock**: Simulação controlada de componentes reais
- Objetivo: Isolar a classe sendo testada de dependências externas
- **Escopo**: Exclusivo para teste unitário

## Características dos Mocks

- Possuem **comportamento previsível** e controlado
- **Imitam interfaces** de componentes reais
- Fornecem **respostas consistentes** para testes
- **Validam interações** com as dependências

## Quando Usar Mocks

- ✅ **Acesso a recursos externos** (APIs, bancos de dados)
- ✅ **Operações lentas** ou de alto custo
- ✅ **Cenários de erro** difíceis de reproduzir
- ✅ **Componentes não implementados** ainda
- ✅ **Testes determinísticos** que não podem falhar aleatoriamente

## Tipos de Objetos de Teste (Padrões xUnit)

- **Mock**: Verifica **comportamento** (se métodos foram chamados)
- **Stub**: Fornece **respostas pré-definidas**
- **Fake**: Implementação simplificada funcional
- **Dummy**: Objeto placeholder sem comportamento

## Vantagens dos Mocks

- **Testes mais rápidos** (sem I/O real)
- **Maior isolamento** e confiabilidade
- **Melhor cobertura** de cenários edge cases
- **Detecção precoce** de bugs de integração

## Desvantagens e Cuidados

- ❗ **Pode mascarar bugs** de integração real
- ❗ **Testes muito acoplados** à implementação
- ❗ **Manutenção custosa** se interface mudar frequentemente
- ❗ **Falsos positivos** se mock não refletir comportamento real

## Boas Práticas

- Mock apenas **dependências externas**, não domínio principal
- Prefira **mocks baseados em interfaces** não em classes concretas
- **Valide interações** importantes, mas evite over-specification
- **Use frameworks** apropriados (Mockito, Jest, etc.)    
- **Combine com testes de integração** para validação completa

## Exemplo Prático

```java
// Sem mock (teste de integração)
servicoReal.chamarAPIExterna() // Lento e instável

// Com mock (teste unitário)
mockAPI.quando(chamarEndpoint()).retornar(respostaMock)
servicoTestado.executar() // Rápido e confiável
```

## Frameworks Populares

- **Java**: Mockito, EasyMock
- **JavaScript/TypeScript**: Jest, Sinon.js
- **Python**: unittest.mock, pytest-mock
- **C#**: Moq, NSubstitute

## Métricas Importantes

- **Tempo de execução** dos testes (deve ser rápido)
- **Cobertura de código** alcançada com mocks
- **Confiabilidade** dos testes (taxa de falsos positivos/negativos)

[[Teste de Unidade]] | [[Teste de Integração]] | [[TDD]] | [[Design Patterns]]