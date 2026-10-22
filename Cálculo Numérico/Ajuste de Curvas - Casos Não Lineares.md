- Casos em que eu faço o ajuste usando funções não lineares, como uma exponencial, logaritmo, etc
- No ajuste, eu não preciso que minha curva passe por todos os pontos, mas um bom ajuste passa o mais perto possível de todos os pontos
## Motivação
- As vezes o sistema pode ser descrito por uma função que não segue uma função polinomial, como decaimento radioativo e crescimento populacional
- Para se aplicar o métodos dos mínimos quadrados é necessário efetuar uma **linearização**
- A opção pelo ajuste de curvas para casos não lineares é feita pela observação do gráfico de dispersão dos dados fornecidos
- Ao fazer a linearização, a variável é trocada para ser possível usar o método dos mínimos quadrados
	- $$y = a\cdot e^{bx}$$
	- $$y \to ln(y) $$
	- $$a\cdot e^{bx} \to \ln{a} + bx$$
	- $$ z = \ln{y}$$
	- $$a_0 = \ln a$$
	- $$ a_{1} = b$$
	- Ficando com:
		- $$ z = a_{0} + a_{1} x$$
> Para os casos não lineares, sempre se troca a tabela