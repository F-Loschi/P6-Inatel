## Definições Fundamentais

### Variáveis em Interpolação
- **Variável independente (x)**: Valor que ajustamos/controlamos no problema
- **Variável dependente (y = f(x))**: Valor que medimos e que depende da variável independente

### Conceitos Básicos
- **Interpolação**: Estimar valores de f(x) para pontos **dentro** do intervalo medido
- **Extrapolação**: Estimar valores de f(x) para pontos **fora** do intervalo medido
- **Função interpoladora g(x)**: Função que aproxima f(x) baseada nos pontos conhecidos

## Necessidade de Interpolação
- Quando uma função é **muito complicada** e dificulta operações de derivação e integração
- Quando se dispõe apenas de **alguns valores discretos** de f(x)
- Quando a função original é **desconhecida**, mas temos pontos experimentais
- Para **simplificar computações** complexas

## Interpolação Polinomial

### Princípio Básico
- A função interpoladora g(x) é um **polinômio**
- g(x) passa **obrigatoriamente** por todos os pontos conhecidos de f(x)
- Quanto mais pontos, maior o grau do polinômio interpolador
- Exemplo:
![[Pasted image 20250909183650.png]]
### Método de Resolução

#### 1. Definição do Polinômio
$$
g(x) = a_nx^n + a_{n-1}x^{n-1} + \cdots + a_1x + a_0
$$
- Para n+1 pontos, usamos um polinômio de grau n

#### 2. Sistema de Equações Lineares
Criamos um sistema onde cada ponto (xᵢ, yᵢ) gera uma equação:
$$
a_nx_i^n + a_{n-1}x_i^{n-1} + \cdots + a_1x_i + a_0 = y_i

$$

#### 3. Forma Matricial
$$
\begin{bmatrix}
x_0^n & x_0^{n-1} & \cdots & x_0 & 1 \\
x_1^n & x_1^{n-1} & \cdots & x_1 & 1 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
x_n^n & x_n^{n-1} & \cdots & x_n & 1
\end{bmatrix}
\begin{bmatrix}
a_n \\
a_{n-1} \\
\vdots \\
a_0
\end{bmatrix}
=
\begin{bmatrix}
y_0 \\
y_1 \\
\vdots \\
y_n
\end{bmatrix}
$$

#### 4. Resolução do Sistema
- **Eliminação Gaussiana**
- **Decomposição LU**
- **Métodos iterativos**
- **Fórmulas específicas** (Lagrange, Newton)

#### 5. Verificação da Solução
- Avaliar g(x) nos pontos conhecidos
- Calcular resíduos |f(xᵢ) - g(xᵢ)|
- Analisar qualidade da aproximação

## Escolha dos Pontos

### Estratégias de Seleção
- **Pontos igualmente espaçados**: Simples, mas pode causar instabilidade (Fenômeno de Runge)
- **Pontos de Chebyshev**: Minimizam o erro de interpolação
- **Baseados na função**: Maior densidade onde a função varia mais

### Considerações Importantes
- **Número de pontos**: Mais pontos → melhor aproximação, mas maior custo computacional
- **Distribuição**: Deve refletir o comportamento da função
- **Condicionamento**: Matriz de Vandermonde pode ser mal-condicionada

## Métodos Alternativos de Interpolação

### Polinômio de Lagrange
- Evita resolver sistema linear
- Fórmula direta: 
- $$
g(x) = \sum_{i=0}^n y_i \cdot L_i(x)
$$
onde 
$$
L_i(x) = \prod_{\substack{j=0 \\ j \neq i}}^n \frac{x - x_j}{x_i - x_j}
$$

### Diferenças Divididas de Newton
- Mais eficiente computacionalmente
- Fácil adição de novos pontos
- Forma:
$$
g(x) = f[x_0] + f[x_0,x_1](x-x_0) + \cdots + f[x_0,\ldots,x_n](x-x_0)\cdots(x-x_{n-1})
$$

## Aplicações Práticas
- **Processamento de sinais**: Reconstrução de sinais amostrados
- **Computação gráfica**: Renderização de curvas e superfícies
- **Análise numérica**: Integração e diferenciação numérica
- **Ciência de dados**: Preenchimento de dados missing

## Limitações e Cuidados
- **Fenômeno de Runge**: Oscilações em extremos com pontos igualmente espaçados
- **Overfitting**: Polinômio de grau muito alto pode seguir ruídos
- **Extrapolação perigosa**: Comportamento imprevisível fora do intervalo
- **Custo computacional**: O(n³) para resolver o sistema linear

## Exemplo Prático
Dados pontos: (0,1), (1,3), (2,7)
Polinômio interpolador: g(x) = x² + x + 1
Verificação: g(0)=1, g(1)=3, g(2)=7 ✓

---

*Nota: A interpolação é ferramenta poderosa, mas deve ser usada com entendimento de suas limitações e pressupostos.*

[[Métodos Numéricos]] | [[Ajuste de Curvas]] | [[Sistemas Lineares]] | [[Análise de Erros]]