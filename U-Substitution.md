#Calculus #Math
If $f(x)=(x^3+5)^5$, find $f^\prime (x)$
$$f^\prime(x)=5(x^3+5)^4(3x^2)=15x^2(x^3+5)^4$$
Since we know the [[chain rule]] pattern, wee should be able to do it in reverse
$$\int2x(x^2+1)^2dx=\frac{1}{3}(x^2+1)^3$$
Formal notation: start with chain rule
$$\frac{d}{dx}[f(g(x))]=f^\prime(g(x))\cdot g^\prime(x)$$
Use $F(x)$ instead of $f(x)$:
$$\frac{d}{dx}[F(g(x))]=F^\prime(g(x))\cdot g^\prime(x)$$
$$\int f(g(x))\cdot g^\prime(x) dx=F(g(x))+C$$
>[!definition]
>u-Substitution Formal Procedure
>$$\int2x(x^2+1)^2dx$$
>$$\text{let}\;u = x^2+1$$
>$$\frac{d}{dx}[u=x^2+1]=\frac{du}{dx}=2x$$
>$$du=2xdx$$
>$$\int u^2du=\frac{1}{3}(x^2+1)^3+C$$
>$$=\frac{1}{3}(x^2+1)^3+C$$
>