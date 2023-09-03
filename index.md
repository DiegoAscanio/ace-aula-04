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

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
  }
  img[alt=grid-img] {
    width: 100%;
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

- Toda função matemática é linear quando ela é FECHADA na adição (propriedade da aditividade - superposição) e na multiplicação por escalar (propriedade da homogeneidade).
    - FECHADA implica dizer que ao adicionar funções lineares ou multiplicar uma função linear por um valor escalar produzo outra função linear resultante (Conceitos oriundos da álgebra linear, não serão desenvolvidos a fundo por fugirem do escopo da disciplina).

- A função da Lei de Ohm, representada por \\(V(t) = Ri(t)\\) é uma função linear (da forma \\(y = ax + b)\\).
- Assim, pelos princípios da sobreposição e linearidade, circuitos elétricos resistivos (capacitivos e indutivos em situações específicas) são equivalentes a sistemas de equações lineares.
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
