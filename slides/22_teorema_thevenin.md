## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element regular">

### Algoritmo para simplificação de circuitos com fontes dependentes.

1. Identificar elementos do circuito a serem simplificados
2. Cálculo de \\(R_{\text{TH}}\\):
    1. Curto circuitar fontes independentes de tensão;
    2. Remover fontes independentes de corrente;
    3. Adicionar fonte de tensão virtual \\(V_{0}\\) entre os terminais \\(a\\) e \\(b\\) do circuito.
    4. Atribuir correntes para os elementos do circuito, inclusive para as fontes dependentes de tensão.
    5. Atribuir tensões para os elementos do circuito, inclusive para as fontes dependentes de corrente, considerar a lei de Ohm para atribuição da tensão dos elementos de resistência.
    6. Resolver as equações do circuito para encontrar a relação \\(R_{\text{TH}} = {{V_{0}} \over {i_{0}}}\\)

</div>
<div class="grid-element regular">

### Algoritmo para simplificação de circuitos com fontes dependentes.
3. Cálculo de \\(V_{\text{TH}}\\):
    1. Retornar as fontes independentes para o circuito.
    2. Atribuir correntes para os elementos do circuito, inclusive para as fontes de tensão.
    3. Atribuir tensões para os elementos do circuito, inclusive para as fontes de corrente, considerar a lei de Ohm para atribuição da tensão dos elementos de resistência.
    4. Resolver as equações do circuito para encontrar as tensões e correntes dos elementos e a tensão de Thévenin, presente entre os terminais \\(a\\) e \\(b\\).
4. Construa o circuito equivalente de Thévenin quando necessário.

</div>
</div>
