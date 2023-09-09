## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="regular">

### Passo 3 - Cálculo de \\(R_{\text{TH}}\\)

Observamos que Existem 8 variáveis desconhecidas, porém, apenas 7 equações, o que é esperado, pois, adicionamos uma fonte virtual \\(V_{0}\\) que apresenta uma corrente virtual \\(i_{0}\\). Escrever um sistema linear para estas equações e considerar \\(i_{0}\\) como a variável com grau de liberdade é suficiente para encontrar \\(R_{\text{TH}}\\), pois, será possível relacionar \\(V_{0}\\) à \\(i_{0}\\).

</div>

<div class="regular">

Assim, o sistema linear composto pelas 7 equações (e uma linha nula para a equação ausente) é representado pela seguinte matriz:

\\[
\left[\begin{matrix}0 & 0 & 1.0 & 0 & 0 & 0 & -8.0 & 0 & 0\\\\0 & 1.0 & 0 & 0 & 0 & -2.0 & 0 & 0 & 0\\\\0 & 0 & 0 & 0 & 1.0 & 0 & -3.0 & 0 & 0\\\\0 & 0 & 0 & 0 & 0 & -1.0 & -4.0 & 1.0 & 0\\\\0 & 0 & 0 & 1.0 & 0 & 0 & -8.0 & 0 & 0\\\\0 & 0 & 0 & 0 & 0 & 2.0 & -8.0 & 0 & 0\\\\1.0 & 0 & 0 & 0 & 0 & -2.0 & 0 & 0 & 0\\\\0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\end{matrix}\right] \cdot \left[\begin{matrix}V_{C}\\\\V_{B}\\\\V_{A}\\\\V_{0}\\\\i_{3}\\\\i_{2}\\\\i_{1}\\\\i_{0}\end{matrix}\right] = \left[\begin{matrix}0\\\\0\\\\0\\\\0\\\\0\\\\0\\\\0\\\\0\end{matrix}\right]
\\]

</div>
