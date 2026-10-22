## Conceito Fundamental
- No ajuste de curvas, o polinômio de ajuste **não necessariamente passa por todos os pontos** tabelados, diferentemente da interpolação
- Objetivo: Encontrar a curva que **melhor se aproxima** do conjunto de pontos, minimizando o erro total

## Por que Utilizar Ajuste de Curvas?
- Para conjuntos com **muitos pontos**, a interpolação se torna complexa e computacionalmente custosa
- Permite encontrar um polinômio de **qualquer grau** que se ajuste aos dados
- O grau do polinômio pode ser escolhido através da **observação do gráfico de dispersão**
- Ideal para dados experimentais com **ruído ou erros de medição**

## Comparativo: Interpolação vs. Ajuste

### Interpolação Polinomial
- ✅ **Passa obrigatoriamente por todos os pontos**
- ✅ Grau determinado pelo número de pontos (n pontos → grau n-1)
- ✅ Solução exata para os pontos dados
- ❌ Problemas com muitos pontos (fenômeno de Runge)
- ❌ Sensível a erros experimentais

### Ajuste de Curvas
- ✅ **Não necessariamente passa por todos os pontos**
- ✅ Grau escolhido pelo analista (baseado no gráfico de dispersão)
- ✅ Minimiza o erro global (método dos mínimos quadrados)
- ✅ Melhor para dados com ruído ou tendências
- ✅ Mais estável com muitos pontos

## Características Matemáticas

### Princípio dos Mínimos Quadrados
- Minimiza a soma dos quadrados dos resíduos:
  $$
  S = \sum_{i=1}^{m} [y_i - f(x_i)]^2
  $$
- A soma dos desvios deve tender a zero
- Encontra os coeficientes que melhor representam a tendência dos dados

### Sistema Normal para Ajuste Polinomial

$$
\begin{bmatrix}
m & \sum x_i & \sum x_i^2 & \sum x_i^3 & \cdots & \sum x_i^n \\
\sum x_i & \sum x_i^2 & \sum x_i^3 & \sum x_i^4 & \cdots & \sum x_i^{n+1} \\
\sum x_i^2 & \sum x_i^3 & \sum x_i^4 & \sum x_i^5 & \cdots & \sum x_i^{n+2} \\
\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
\sum x_i^n & \sum x_i^{n+1} & \sum x_i^{n+2} & \sum x_i^{n+3} & \cdots & \sum x_i^{2n}
\end{bmatrix}
\begin{bmatrix}
a_0 \\
a_1 \\
a_2 \\
\vdots \\
a_n
\end{bmatrix}
=
\begin{bmatrix}
\sum y_i \\
\sum x_i \cdot y_i \\
\sum x_i^2 \cdot y_i \\
\vdots \\
\sum x_i^n \cdot y_i
\end{bmatrix}
$$

**Onde:** 
- $m$ = número de pontos
- $n$ = grau do polinômio de ajuste

## Metodologia Passo a Passo

### 1. Escolha do Grau do Polinômio
- Analise o **gráfico de dispersão** dos pontos
- Identifique o **comportamento** (linear, quadrático, exponencial, etc.)
- Exemplo para ajuste linear: 
  $$
  \hat{y}(x) = a_0 + a_1x
  $$

### 2. Montagem do Sistema de Equações
- Para ajuste linear:
  $$
  \begin{bmatrix} 
  m & \sum x_k \\ 
  \sum x_k & \sum x_k^2 
  \end{bmatrix} 
  \begin{bmatrix} 
  a_0 \\ 
  a_1 
  \end{bmatrix} 
  = 
  \begin{bmatrix} 
  \sum y_k \\ 
  \sum x_k y_k 
  \end{bmatrix}
  $$

### 3. Construção da Tabela de Cálculos
$$
\begin{array}{|c|c|c|c|c|c|}
\hline
k & x_k & x_k^2 & x_k^3 & y_k & x_k \cdot y_k \\
\hline
1 & x_1 & x_1^2 & x_1^3 & y_1 & x_1 y_1 \\
2 & x_2 & x_2^2 & x_2^3 & y_2 & x_2 y_2 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
m & x_m & x_m^2 & x_m^3 & y_m & x_m y_m \\
\hline
\sum & \sum x_k & \sum x_k^2 & \sum x_k^3 & \sum y_k & \sum x_k y_k \\
\hline
\end{array}
$$

### 4. Cálculo dos Somatórios
- Preencher a tabela com os valores
- Calcular todas as somas necessárias
- Quanto maior o grau, mais colunas serão necessárias

### 5. Resolução do Sistema Linear
- Resolver o sistema para encontrar os coeficientes $a_0, a_1, \ldots, a_n$
- Usar métodos como eliminação gaussiana ou decomposição LU

### 6. Verificação da Qualidade do Ajuste
- Calcular o **coeficiente de determinação** ($R^2$)
- Analisar os **resíduos** (diferenças entre valores reais e previstos)
- $$
  R^2 = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}
  $$

## Exemplo Prático: Ajuste Linear

### Dados:
```
Pontos: (1, 2), (2, 3), (3, 5), (4, 4), (5, 6)
```

### Tabela de Cálculos:
$$
\begin{array}{|c|c|c|c|c|}
\hline
k & x_k & x_k^2 & y_k & x_k y_k \\
\hline
1 & 1 & 1 & 2 & 2 \\
2 & 2 & 4 & 3 & 6 \\
3 & 3 & 9 & 5 & 15 \\
4 & 4 & 16 & 4 & 16 \\
5 & 5 & 25 & 6 & 30 \\
\hline
\sum & 15 & 55 & 20 & 69 \\
\hline
\end{array}
$$

### Sistema Linear:
$$
\begin{bmatrix} 
5 & 15 \\ 
15 & 55 
\end{bmatrix} 
\begin{bmatrix} 
a_0 \\ 
a_1 
\end{bmatrix} 
= 
\begin{bmatrix} 
20 \\ 
69 
\end{bmatrix}
$$

### Solução:
$$
\hat{y}(x) = 1.1 + 0.9x
$$

## Escolha do Melhor Grau

### Técnicas de Seleção
- **Análise visual** do diagrama de dispersão
- **Coeficiente de determinação** ($R^2$)
- **Análise de resíduos** (devem ser aleatórios)
- **Critérios de informação**: AIC, BIC
- **Validação cruzada** para evitar overfitting

## Aplicações do Ajuste de Curvas
- **Análise de dados experimentais**
- **Previsões e tendências**
- **Suavização de dados ruidosos**
- **Modelagem de fenômenos físicos**
- **Machine learning** (regressão linear/polinomial)

## Vantagens e Limitações

### Vantagens
- ✅ **Robusto** contra ruídos nos dados
- ✅ **Flexibilidade** na escolha do grau
- ✅ **Interpretabilidade** dos resultados
- ✅ **Computacionalmente eficiente**

### Limitações
- ❌ **Subjetividade** na escolha do grau
- ❌ **Overfitting** se grau for muito alto
- ❌ **Underfitting** se grau for muito baixo
- ❌ **Pressupõe forma funcional** conhecida

---

**[[Métodos Numéricos]]** | **[[Interpolação Polinomial]]** | **[[Sistemas Lineares]]** | **[[Análise de Dados]]** | **[[Regressão Estatística]]**