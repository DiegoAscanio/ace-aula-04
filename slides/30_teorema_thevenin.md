## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="grid-50-50 normal">

<div class="grid-element">

Identificando os elementos do sistema, as correntes que circulam por si, suas tensões, os nós e as malhas do circuito, temos:

<center>
<img src="./img/circuito-a-ser-simplificado-com-fonte-dependente-de-corrente-rotulado.png" class="transparent"> 
</center>

Agora, precisamos construir as equações.

</div>

<div class="grid-element small">

No nó \\(N_{1}\\) entram zero correntes e saem: \\(i_{0}, i_{1}, i_{3} \text{ e } i_{4}\\). Sabemos também que \\(i_{1} = 4A\\). Portanto:

<div class="grid-50-50 footnotesize">
<div class="grid-element">

\\[
\begin{equation}
i_{4} - 3 i_{0} = 0 \\\\
i_{0} + i_{3} + i_{4} = -4 \\\\
i_{0} - i_{2} = -4 \\\\
V_{b} - 2 i_{3} = 24 
\end{equation}
\\]

</div>
<div class="grid-element">

\\[
\begin{equation}
V_{d} - 2 i_{3} = 0 \\\\
V_{b} - 8 i_{0} = 0 \\\\
V_{a} - 8 i_{0} = 0 \\\\
V_{c} - 2 i_{3} = 0
\end{equation}
\\]

</div>

</div>

Temos 8 símbolos desconhecidos e 8 equações, logo, conseguimos construir um SL, idealmente possível e determinado, representado por:

<div class="footnotesize">

\\[
\left[\begin{matrix}0 & 0 & 0 & 0 & -3.0 & 0 & 0 & 1.0\\\\0 & 0 & 0 & 0 & 1.0 & 0 & 1.0 & 1.0\\\\0 & 0 & 0 & 0 & 1.0 & -1.0 & 0 & 0\\\\0 & 1.0 & 0 & 0 & 0 & 0 & -2.0 & 0\\\\0 & 0 & 0 & 1.0 & 0 & 0 & -2.0 & 0\\\\0 & 1.0 & 0 & 0 & -8.0 & 0 & 0 & 0\\\\1.0 & 0 & 0 & 0 & -8.0 & 0 & 0 & 0\\\\0 & 0 & 1.0 & 0 & 0 & 0 & -2.0 & 0\end{matrix}\right]
{} \cdot {}
\left[\begin{matrix}V_{a}\\\\V_{b}\\\\V_{c}\\\\V_{d}\\\\i_{0}\\\\i_{2}\\\\i_{3}\\\\i_{4}\end{matrix}\right]
{} = {}
\left[\begin{matrix}0\\\\-4.0\\\\-4.0\\\\24.0\\\\0\\\\0\\\\0\\\\0\end{matrix}\right]
\\]

</div>

</div>

</div>
