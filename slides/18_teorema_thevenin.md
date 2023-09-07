## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element regular">

### Passo 4.2

Pelas Lei de Ohm, de Kirchoff da Corrente nos Nós e de Kirchoff das Tensões nas Malhas temos:

<div class="grid-50-50">
<div class="grid-element small">

\\[
\begin{align}
V_{i} - 5 i_{1} &= 0 \\\\
V_{j} - 20 i_{2} &= 0 \\\\
i_{1} - i_{2} &= -3
\end{align}
\\]

</div>
<div class="grid-element small">

\\[
\begin{align}
V_{k} - 20 i_{2} &= 0 \\\\
5 i_{1} + 20 i_{2} &= 25
\end{align}
\\]

</div>

</div>

Que produz o seguinte sistema linear na forma matricial:

<div class="small">

\\[
\begin{bmatrix}
1 & 0 & 0 & -5 & 0 \\\\
0 & 1 & 0 & 0 & -20 \\\\
0 & 0 & 0 & 1 & -1 \\\\
0 & 0 & 1 & 0 & -20 \\\\
0 & 0 & 0 & 5 & 20
\end{bmatrix}
\begin{bmatrix}
V_{i} \\\\
V_{j} \\\\
V_{k} \\\\
i_{1} \\\\
i_{2}
\end{bmatrix}
{ = }
\begin{bmatrix}
0 \\\\
0 \\\\
-3 \\\\
0 \\\\
25
\end{bmatrix}
\\]

</div>

Este sistema linear em sua representação matricial é resolvido no próximo slide.

</div>
<div class="grid-element normal">

<figure>

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-4-2-2.svg)

<figcaption>

Correntes, tensões, sentidos de quedas de potencial, malhas e nós indetificados no circuito.

</figcaption>

</figure>

</div>
</div>
