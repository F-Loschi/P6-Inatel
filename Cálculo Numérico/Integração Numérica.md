### 1. Introdução à Integração Numérica

As **integrais analíticas** são aquelas em que conseguimos obter a **função antiderivada (primitiva)** através de um processo lógico.

No entanto, em alguns casos, o valor dessa primitiva **não é conhecido ou é de difícil obtenção**. Além disso, em situações práticas, a função a ser integrada (f(x)) nem sempre é definida por uma fórmula analítica, mas sim por uma **tabela de pontos**.

Nessas situações, é necessário recorrer à **integração numérica** para encontrar um valor aproximado da integral definida.

---

### 2. Regra do Trapézio (Simples)

Esta regra consiste em substituir a função integrando f(x) por um **polinômio interpolador de grau 1 (uma reta)**, que a interpola nos extremos do intervalo de integração [a,b]. A área sob a curva é então aproximada pela **área de um trapézio**.

A fórmula da aproximação é:
$$
I_{T}​≈2h​[f(a)+f(b)]
$$
Onde h=b−a (largura do intervalo).

#### Erro de Truncamento (ET​)

É a diferença entre o valor da integral exata de f(x) e a integral aproximada pela Regra do Trapézio. Este erro depende da **derivada segunda** da função (f′′(x)) e da largura do intervalo (h).
$$
E_T = -\frac{h^3}{12} f''(c), \qquad a \leq c \leq b
$$
Onde c é um valor no intervalo [a,b] que maximiza o erro (geralmente, o máximo valor da derivada segunda no intervalo).

O valor exato da integral é dado por I=IT​+ET​.

**Exemplo de Aplicação (Passos):** Para calcular$$I = \int_{3.0}^{3.6} \frac{dx}{x}$$pela Regra do Trapézio:

1. Fazer a tabela dos valores de x e f(x) nos extremos a=3.0 e b=3.6.
    
2. Calcular o valor de h=b−a.
    
3. Usar a fórmula do trapézio (IT​).
    
4. Calcular a **derivada segunda** de f(x).
    
5. Encontrar o valor de c (que pode ser a ou b) que maximize ∣f′′(c)∣.
    
6. Calcular o **erro de truncamento** (ET​).
    
7. Somar o valor da integração com o erro de truncamento para obter a integral exata I=IT​+ET​.
    

---

### 3. Regra dos Trapézios Repetida

Quanto maior o intervalo de integração [a,b], maior é o erro cometido pela Regra do Trapézio simples.

Para minimizar o erro, subdividimos o intervalo em n **subintervalos** de amplitude h=nb−a​ (partes iguais) e aplicamos a Regra do Trapézio a cada subintervalo.

A fórmula da aproximação é:
$$
I_{TR} \approx \frac{h}{2} \left[ f(x_0) + 2f(x_1) + 2f(x_2) + \ldots + 2f(x_{n-1}) + f(x_n) \right]
$$
Onde x0​=a e xn​=b. Note que apenas os pontos extremos (x0​ e xn​) têm o coeficiente 1, enquanto os pontos internos são multiplicados por 2.

#### Erro de Truncamento Repetido (ETR​)

Ao usar n trapézios, o erro total é a soma dos erros de truncamento de cada subintervalo:
$$
ETR​=ET1​+ET2​+…+ETn​
$$
A fórmula simplificada do erro de truncamento da Regra dos Trapézios Repetida é:
$$
E_{TR} = E_{T1}+ E_{T2} + \ldots + E_{Tn}
$$
$$
E_{TR} = -\frac{(b - a)^3}{12n^2} \, f''(c)
$$
Onde n é o número de subintervalos. **Quanto maior o número de subintervalos (n), menor o erro.**

---

### 4. Regra de Simpson (Simples)

A Regra de Simpson simples consiste em substituir a função integrando f(x) por um **polinômio interpolador de grau 2 (uma parábola)**, que a interpole em 3 pontos igualmente espaçados: x0​=a, x1​=a+h, e x2​=a+2h=b.

Neste caso, a largura do subintervalo é h=2b−a​.

A fórmula da aproximação é:

$$
I_s = \frac{h}{3} \left[ f(x_0) + 4f(x_1) + f(x_2) \right]
$$

O **erro de truncamento** (ES​) é dado por:

$$
E_s = -\frac{h^5}{90} f^{(4)}(c)
$$
Onde f(4)(c) é o valor máximo da derivada de ordem 4 no intervalo [a,b].

O valor exato da integral é
$$
I = I_s + E_s
$$

---

### 5. Regra de Simpson Repetida

Para aumentar a precisão, dividimos o intervalo de integração [a,b] em n **subintervalos** (onde **n deve ser um número par**) de amplitude h=nb−a​. Aplicamos a Regra de Simpson a cada **par** de subintervalos.

A fórmula da aproximação é:
$$
I_{SR} = \frac{h}{3} \left[ f(x_0) + 4f(x_1) + 2f(x_2) + 4f(x_3) + 2f(x_4) + \cdots + 2f(x_{n-2}) + 4f(x_{n-1}) + f(x_n) \right]
$$
Note a sequência de coeficientes: **1, 4, 2, 4, 2, ..., 4, 1**.

O **erro de truncamento** (ESR​) é dado por:

$$
E_{SR} = -\frac{(b - a)^5}{180 n^4} f^{(4)}(c)
$$

O valor exato da integral é 
$$
I = I_{SR} + E_{SR}
$$

---

### 6. Considerações Finais sobre as Regras

|Regra|Complexidade/Cálculo|Precisão|
|---|---|---|
|**Trapézio (Simples)**|Mais simples e rápido de calcular.|Menor precisão (erro ∝h3 e f′′).|
|**Trapézios Repetidos**|Um pouco mais de trabalho no cálculo.|Precisão um pouco maior que a simples (erro ∝1/n2).|
|**Simpson (Simples)**|Mais complicado que o Trapézio. Cálculo mais lento.|Precisão maior (erro ∝h5 e f(4)).|
|**Simpson Repetida**|Mais complicado de calcular e maior chance de erro na aplicação da fórmula.|Precisão ainda maior que o Simpson simples (erro ∝1/n4).|

**Importante:** É fundamental ter muito cuidado com as **fórmulas** para não confundir os coeficientes e as potências do h em cada regra e erro.