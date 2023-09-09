<style>
  section {
    background: #fff url(./img/background.png) no-repeat center center;
    background-size: cover;
  }

  .transparent {
    background-color: transparent!important;
  }

  section.transparent img {
    background-color: transparent!important;
  }

  .transparent-table-tr-td-th {
    background-color: rgba(0, 0, 0, 0.0) !important;
  }

  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }

  .conteudo {
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }

  .conteudo-absoluto {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
  
  .large {
    font-size: 36px;
  }

  .normal {
    font-size: 22px;
  }
  .regular {
    font-size: 18px;
  }
  .small {
    font-size: 16px;
  }
  .footnotesize {
    font-size: 14px;
  }
  .scriptsize {
    font-size: 12px;
  }
  .tiny {
    font-size: 10px;
  }
  .bold {
    font-weight: bold;
  }
  .center {
    text-align: center;
  }
  section.lead p {
    text-align: justify;
  }
  section.lead h1 {
    text-align: center;
  }
  section.lead h2 {
    text-align: center;
  }
  .two-columns-33-66 {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    display: grid;
    grid-template-columns: 1fr 2fr;
    font-size: 28px;
    text-align: justify;
  }
  .two-columns-66-33 {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    display: grid;
    grid-template-columns: 2fr 1fr;
    font-size: 28px;
    text-align: justify;
  }

  .two-columns-50-50 {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    font-size: 28px;
    text-align: justify;
  }

  .grid-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: justify;
  }

  .grid-66-33 {
    display: grid;
    grid-template-columns: 2fr 1fr;
    text-align: justify;
  }

  .grid-33-66 {
    display: grid;
    grid-template-columns: 1fr 2fr;
    text-align: justify;
  }

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
  }
  img[alt=grid-img] {
    width: 100%;
  }

  .grid-element-mid-aligned {
    width: 100%;
    margin-top: 25%;
    margin-bottom: 25%;
  }

</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>


# Análise de Circuitos Elétricos
## Aula 04 - Teoremas de Thévernin e Norton
 
Prof. M.Sc. Diego Ascânio Santos (ascanio@cefetmg.br)

Aula baseada sobre o material da professora Drª. Jossana Maria de Souza Ferreira (jossana.ferreira@ufrn.br - ECT - ESCOLA DE CIÊNCIAS E TECNOLOGIA UFRN) e da professora Drª. Thabatta Moreira Alves de Araújo (thabatta@cefetmg.br - DIGDDV)

CEFET-MG DIGDDV - Divinópolis, 2023.


---

<!-- _class: lead -->
# Disclaimer

<!-- _class: lead -->
## Explicit is better than implicit.

<center>
Estes slides obedecem a este princípio.
</center>


---

## Roteiro

1. Fontes dependentes de corrente e de tensão;
2. Linearidade e sobreposição;
3. Homogeneidade, Sobreposição e a Produção de Circuitos Equivalentes;
4. Teorema de Thévenin;
5. Construção de circuitos equivalentes pelo teorema de Thévenin;
6. Teorema de Norton;
7. Construção de circuitos equivalentes pelo teorema de Norton;


---

## Fontes Dependentes

<div class="grid-66-33">

<div class="grid-element regular">

- Fontes de tensão e corrente são ditas independentes quando não são influenciadas por qualquer outra corrente ou tensão no circuito. 
    - Sua representação gráfica consiste em um circulo com os pólos positivo e negativo (quando se trata de uma fonte de tensão) ou um circulo com uma seta (quando se trata de uma fonte de corrente).

- Quando os valores de uma fonte de tensão ou corrente são determinados por outra tensão ou corrente do circuito, então dizemos que estas fontes são dependentes.
    - Na imagem da fonte dependente de tensão (corrente), verificamos que sua tensão \\(V_{s} = 3 V_{x}\\) (corrente \\(i_{s} = 3 V_{x}\\)) é dependente da tensão \\(V_{x} = 5V\\) presente entre os pontos \\(a\\) e \\(b\\) do circuito, onde \\(V_{x}\\) também corresponde à tensão da fonte de tensão independente do circuito.

- A representação gráfica das fontes dependentes consistem em um losango contendo pólos \\(-\\) quando a fonte dependente fornece tensão \\(-\\) ou um losango contendo uma seta \\(-\\) quando a fonte dependente fornece corrente.


</div>

<div class="grid-element regular">

<center>
<figure>

<!-- _class: transparent -->
![](img/fonte-dependente-tensao.png)

<figcaption>Circuito com fonte dependente de Tensão</figcaption>

</figure>

<figure>

![](img/fonte-dependente-corrente.png)

<figcaption>Circuito com fonte dependente de Corrente</figcaption>

</figure>
</center>

</div>

</div>


---

## Linearidade e Superposição

<div class="normal" >

- Toda função matemática é linear quando ela é FECHADA na adição (propriedade da aditividade - superposição) e na multiplicação por escalar (propriedade da homogeneidade - linearidade).
    - FECHADA implica dizer que ao adicionar funções lineares ou multiplicar uma função linear por um valor escalar produzo outra função linear resultante (Conceitos oriundos da álgebra linear, não serão desenvolvidos a fundo por fugirem do escopo da disciplina).

- A função da Lei de Ohm, representada por \\(V(t) = Ri(t)\\) é uma função linear (toda função linear é da forma \\(y = ax + b)\\).
- Assim, pelos princípios da superposição e linearidade, circuitos elétricos resistivos (capacitivos e indutivos em situações específicas) são equivalentes a sistemas de equações lineares.
    - Por isso, conseguimos resolver circuitos usando sistemas lineares.

</div>


---

## Homogeneidade, Sobreposição e a Produção de Circuitos Equivalentes

<div class="regular" >

- A homogeneidade nos ajuda a atribuir arbitrariamente valores para elementos dos circuitos e, consequentemente, deduzir demais grandezas, por garantir que as multiplicações por valores escalares persistem a produzir elementos lineares.

- A sobreposição de circuitos nos permite deduzir que a as grandezas de um elemento podem ser calculadas levando-se em consideração a contribuição individual de elementos de circuito sobre eles, pois, a propriedade da adição garante que a adição de funções lineares continua a produzir outra função linear.

- Diante disso tudo, estes princípios nos permitem deduzir (e verificar) a existência de circuitos equivalentes, pois, ao garantirem que a sobreposição e homogeneidade produzem funções lineares, logo, formas distintas de se produzirem o mesmo circuito se equivalem.
    - Estas considerações representam tão somente embasamentos teóricos para garantir a validade das operações a serem vistas nos próximos slides. Sua discussão na disciplina se encerra neste slide e estas considerações não são objetos de avaliação do conhecimento da disciplina, pois, reiterando, estão aqui apenas para servir de alicerce \\(-\\) demonstrar a base que permite a existência de circuitos equivalentes, bem como, dos teoremas de Thévenin e Norton, abordados na sequência.

</div>


---

<!-- _class: lead -->
# Teorema de Thévenin


---

## Teorema de Thévenin

<div class="grid-66-33">

<div class="grid-element small">

- O Teorema de Thévenin é um teorema para a simplificação de circuitos que estabelece que:
    - Quaisquer elementos lineares de circuitos entre dois terminais \\(a\\) e \\(b\\) podem ser substituídos por um circuito elétrico equivalente composto por uma fonte de tensão de Thévenin \\((V_{\text{TH}})\\) em série a uma resistência de Thévenin \\((R_{\text{TH}})\\).
    - Porque isto é útil? Porquê nos permite simplificar grandes circuitos complexos em um simples circuito de fonte de tensão e resistência em série que permite facilitar a análise de elementos específicos em um circuito, principalmente, no caso em que desejamos modificar um elemento específico de um circuito (uma resistência \\(R_{L}\\) por exemplo) várias vezes em sequência.
    - Ao mudar os valores de \\(R_{L}\\) várias vezes, sem qualquer tipo de técnica de simplificação do circuito, é necessário reescrever todo o sistema de equações que representa o circuito, pois, uma mudança em um elemento implica uma mudança em uma ou mais equações do sistema.
- Reiterando, o Teorema de Thévenin consiste em substituir uma parte do circuito cujos detalhes não interessam por um circuito equivalente formado por uma fonte de tensão \\((V_{\text{TH}})\\) em série a uma resistência de Thévenin \\((R_{\text{TH}})\\).

</div>

<div class="grid-element small">

<figure>

<!-- _class: transparent -->
![](img/equivalencia-1.png)

<figcaption>Exemplo de circuito que pode ser simplificado</figcaption>
</figure>

<figure>

<!-- _class: transparent -->
![](img/equivalencia-2.png)

<figcaption>

Simplificação proposta para os componentes do circuito entre os terminais \\(a\\) e \\(b\\) por meio de circuito equivalente de Thévenin

</figcaption>
</figure>


</div>

</div>


---

## Teorema de Thévenin - Como Aplicar?

<div class="normal">

Reiterando: a aplicação do Teorema de Thévenin consiste na substituição de um circuito de maior complexidade com múltiplos elementos presente entre dois terminais \\(a\\) e \\(b\\) por um circuito simples que consiste em uma fonte de tensão de Thévenin em série a uma resistência de Thévenin:

</div>

<div class="grid-50-50 regular">

<div class="grid-element">
<figure>

<!-- _class: transparent -->
![](img/circuito-complexo.png)

<figcaption>

Circuito de maior complexidade entre terminais \\(a\\) e \\(b\\)

</figcaption>

</figure>
</div>

<div class="grid-element">
<figure>

<!-- _class: transparent -->
![](img/circuito-equivalente-thevenin.png)

<figcaption>

Circuito simplificado equivalente Thévenin entre terminais \\(a\\) e \\(b\\)

</figcaption>

</figure>
</div>

</div>

<div class="normal">

Destarte, nosso objetivo passa a ser encontrar os valores da resistência de Thévenin e da tensão de Thévenin. Como encontrá-los?

</div>


---

<!-- _class: lead -->
# Construção de Circuitos Equivalentes Pelo Teorema de Thevenin


---

## Construção de Circuitos Equivalentes Pelo Teorema de Thévenin - Algoritmo

<div class="normal">

1. Definir qual ponto do circuito a ser simplificado, sinalizado pelos terminais \\(a\\) e \\(b\\).
2. Remover (temporariamente) o resistor \\(R_{L}\\) do circuito.
3. Encontrar a resistência de Thévenin \\(R_{\text{TH}}\\): Zerar apenas as fontes independentes \\(-\\) curto-circuitar as fontes de tensão e abrir as fontes de corrente \\(-\\) e calcular a resistência equivalente deste circuito sem as fontes independentes.
4. Encontrar a tensão de Thévenin \\(V_{\text{TH}}\\) nos terminais \\(a\\) e \\(b\\), considerando a atuação de todas as fontes independentes do circuito. O método estudado da construção de sistemas de equações lineares à partir das LKC, LKT e Lei de Ohm é suficiente.
5. Construir o circuito equivalente de Thévenin adicionando o elemento de carga (aqui representado por \\(R_{L}\\)) de volta ao circuito.

</div>


---

## Equivalente de Thevenin - Exemplo Sem Fontes Dependentes

Substitua os elementos à esquerda dos terminais \\(A\\) e \\(B\\) (que abrangem o resistor \\(R_{L}\\)) por sua fonte e resistência de Thévenin equivalentes.

<center>

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1.svg)

</center>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element">

### Passo 1

Definir qual ponto do circuito a ser simplificado, sinalizado pelos terminais \\(A\\) e \\(B\\).

Definimos que o subcircuito contido na área pontilhada em vermelho, a esquerda dos terminais \\(A\\) e \\(B\\), será o simplificado:

</div>
<div class="grid-element">

<div class="grid-element-mid-aligned">

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-1.svg)

</div>

</div>
</div>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element">

### Passo 2

Removemos temporariamente o resistor \\(R_{L}\\) do circuito.

</div>
<div class="grid-element">

<div class="grid-element-mid-aligned">

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-2.svg)

</div>

</div>
</div>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element normal">

### Passo 3 - Encontrar a Resistência de Thévenin \\(R_{\text{TH}}\\) equivalente.

1. Zeramos somente as fontes independentes
    1. Curto Circuitamos as Fontes de Tensão Independentes
    2. Removemos as Fontes de Corrente Independentes
    3. Calculamos a Resistência Equivalente desta configuração.

\\[
\begin{align}
R_{\text{TH}} &= 4 \Omega + 5 \Omega || 20 \Omega \\\\
R_{\text{TH}} &= 8 \Omega
\end{align}
\\]

</div>
<div class="grid-element">

<div class="grid-element-mid-aligned">

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-3.svg)

</div>

</div>
</div>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element normal">

### Passo 4 - Encontrar a Tensão de Thévenin \\(V_{\text{TH}}\\) nos Terminais \\(A\\) e \\(B\\).

1. Retornamos as fontes de tensão independentes para o circuito.
2. Calculamos pelas leis de Kirchoff da corrente e da tensão, bem como, pela lei de Ohm, as tensões e correntes que passam pelos elementos do circuito.
3. Encontramos \\(V_{\text{TH}}\\).

</div>
<div class="grid-element normal">

<div class="grid-element-mid-aligned">

<figure>

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-4-1.svg)

<figcaption>

Passo \\(4.1\\) - Retorno das fontes independentes ao Circuito

</figcaption>

</figure>

</div>

</div>
</div>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element regular">

### Passo 4.2

<figure>

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-4-1.svg)

<figcaption>

Circuito com o retorno das fontes.

</figcaption>

</figure>


Ao retornar as fontes independentes ao circuito verificamos que não flui corrente no resistor de \\(4 \Omega\\), pois, o terminal \\(A\\) está desconectado. Desta forma, a corrente no resistor de \\(4 \Omega\\) é zero e por isso, o resistor pode ser desconsiderado do circuito para o cálculo da tensão de Thévenin.



</div>
<div class="grid-element regular">

**Mas, ainda assim, existe tensão entre os terminais \\(A\\) e \\(B\\)**

Portanto, o circuito pode ser representado como:


<figure>

<!-- _class: transparent -->
![](./img/thevenin-exemplo-1-passo-4-2-1.svg)

<figcaption>

Passo \\(4.2\\) - Resistor de \\(4 \Omega\\) desconsiderado do Circuito

</figcaption>

</figure>

</div>
</div>


---

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


---

## Resolução do Circuito No JupyterLite pelo SymPy

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=thevenin-sem-fontes-dependentes.ipynb" width=100% height=100%></iframe>


---

## Equivalente de Thévenin - Exemplo Sem Fontes Dependentes

<div class="grid-50-50">
<div class="grid-element regular">

Ao resolver o sistema linear que representa o circuito descobrimos que \\(V_{K} = V_{\text{TH}} = 32 V\\) e assim, finalizamos o passo 4. Com o valor de \\(R_{\text{TH}} = 8 \Omega\\) obtido no passo 3, conseguimos então construir o equivalente de Thévenin (Passo 5) representado a direita, com a volta do elemento \\(R_{L} = 2 \Omega\\) ao circuito.

</div>
<div class="grid-element regular">

<!-- _class: transparent -->
![](./img/circuito-equivalente-thevenin-sem-fonte-dependente.png)

</div>
</div>


---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="small">

Quando existem fontes dependentes de tensão ou de corrente no circuito, aplicamos o mesmo algoritmo para fontes independentes, exceto pelo fato de que não removemos as fontes dependentes do circuito. A existência de elementos dependentes no circuito implica que ao menos uma variável será linearmente dependente de outra, o que pode impedir a resolução do sistema no estado que desejamos: um sistema possível e determinado.

Por isso, nestes casos, convém adicionar ao menos uma fonte de tensão virtual \\(V_{0}\\) percorrida por uma corrente virtual \\(I_{0}\\) entre os terminais \\(A\\) e \\(B\\) onde se deseja encontrar a resistência e a tensão equivalentes de Thévenin. Porquê? Porquê ao admitirmos que se existe uma fonte de tensão \\(V_{0}\\) com uma corrente virtual \\(i_{0}\\) entre os polos \\(A\\) e \\(B\\) onde desejamos construir o equivalente de Thévenin, logo, podemos encontrar a resistência de Thévenin pela lei de Ohm, onde: \\(R_{\text{TX}} = {{V_{0}} \over {I_{0}}}\\) e por consequência, adicionar mais um termo linearmente independente às equações do sistema para conseguirmos calcular os valores exatos, tornando o sistema possível e determinado!

É muito verboso, é muito textual e é necessário algum conhecimento em álgebra linear para o entendimento do raciocínio exposto acima. Entretanto, tudo isso pode ser esquematizado em um simples algoritmo exposto nos próximos slides.

</div>


---

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


---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

Construa o circuito equivalente de Thévenin para o circuito abaixo entre os terminais \\(A\\) e \\(B\\) com uma fonte dependente de corrente que produz uma corrente de \\(3 i_{x}\\).

<center>

<img src="img/circuito-a-ser-simplificado-com-fonte-dependente-de-corrente.png" class="transparent" width="50%">

</center>



---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

### Passo 1 - Identificar elementos para simplificação

<center>

<img src="img/circuito-a-ser-simplificado-com-fonte-dependente-de-corrente.svg" class="transparent" width="50%">

</center>



---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="grid-50-50 small">
<div class="grid-element">

Como não existe elemento a ser removido, passamos diretamente ao passo 3.

### Passo 3 - Cálculo de \\(R_{\text{TH}}\\)

1. Curto circuitar fontes independentes de tensão;
2. Remover fontes independentes de corrente;
3. Adicionar fonte de tensão virtual \\(V_{0}\\) entre os terminais \\(a\\) e \\(b\\) do circuito.
4. Atribuir correntes para os elementos do circuito, inclusive para as fontes dependentes de tensão.
5. Atribuir tensões para os elementos do circuito, inclusive para as fontes dependentes de corrente, considerar a lei de Ohm para atribuição da tensão dos elementos de resistência.


</div>
<div class="grid-element">
<div>

<!-- _class: transparent -->
![](./img/circuito-thevenin-fonte-dependente-de-corrente-sem-fontes-independentes.png)

</div>
<div>

<!-- _class: transparent -->
![](./img/circuito-thevenin-fonte-dependente-simplificado.png)

</div>
</div>
</div>


---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="grid-33-66 regular">

<div class="grid-element">
<img src="./img/circuito-thevenin-fonte-dependente-simplificado.png" class="transparent" style="width: 100%;">
</div>

<div class="grid-element">

### Passo 3 - Cálculo de \\(R_{\text{TH}}\\)

6. Resolver as equações do circuito para encontrar a relação \\(R_{\text{TH}} = {{V_{0}} \over {i_{0}}}\\)

- Na fonte de corrente, definimos para ela uma corrente \\(i_{3}\\), mas, como sabemos que a fonte de corrente produz uma corrente dependente de \\(i_{1}\\) no valor de \\(3 i_{1}\\), logo, \\(i_{3} = 3 i_{1}\\).

Portanto, as seguintes equações podem ser deduzidas deste circuito:

<div class="grid-50-50 small">
<div class="grid-element">

1. \\(V_{A} - 8 i_{1} = 0\\)
2. \\(V_{B} - 2 i_{2} = 0\\)
3. \\(i_{3} - 3 i_{1} = 0\\)

</div>
<div class="grid-element">

4. \\(i_{0} - 4 i_{1} - i_{2} = 0\\)
5. \\(V_{0} - 8 i_{1} = 0\\)
6. \\(- 8 i_{1} + 2 i_{2} = 0\\)
7. \\(V_{C} - 2 i_{2} = 0\\)

</div>
</div>

</div>

</div>


---

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


---

## Resolução do Circuito No JupyterLite pelo SymPy

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=thevenin-com-fonte-dependente.ipynb" width=100% height=100%></iframe>


---

## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="normal">

Após resolver o sistema linear ao fim do passo 3, obtemos \\(R_{\text{TH}} = 1 \Omega\\).

Agora, temos que retornar as fontes independentes ao circuito e calcular a tensão de Thévenin (passo 4) nos terminais \\(A\\) e \\(B\\), representada pela tensão sobre o resistor de \\(8 \Omega\\). Então, devemos aplicar o algoritmo para resolução de circuitos pela LKC, LKT e lei de Ohm para encontrar as tensões e correntes de cada elemento.

<center>
<img src="./img/circuito-a-ser-simplificado-com-fonte-dependente-de-corrente.png" class="transparent" width="40%">
</center>

</div>


---

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
