## Equivalente de Thévenin - Exemplo com Fontes Dependentes

<div class="small">

Quando existem fontes dependentes de tensão ou de corrente no circuito, aplicamos o mesmo algoritmo para fontes independentes, exceto pelo fato de que não removemos as fontes dependentes do circuito. A existência de elementos dependentes no circuito implica que ao menos uma variável será linearmente dependente de outra, o que pode impedir a resolução do sistema no estado que desejamos: um sistema possível e determinado.

Por isso, nestes casos, convém adicionar ao menos uma fonte de tensão virtual \\(V_{0}\\) percorrida por uma corrente virtual \\(I_{0}\\) entre os terminais \\(A\\) e \\(B\\) onde se deseja encontrar a resistência e a tensão equivalentes de Thévenin. Porquê? Porquê ao admitirmos que se existe uma fonte de tensão \\(V_{0}\\) com uma corrente virtual \\(i_{0}\\) entre os polos \\(A\\) e \\(B\\) onde desejamos construir o equivalente de Thévenin, logo, podemos encontrar a resistência de Thévenin pela lei de Ohm, onde: \\(R_{\text{TX}} = {{V_{0}} \over {I_{0}}}\\) e por consequência, adicionar mais um termo linearmente independente às equações do sistema para conseguirmos calcular os valores exatos, tornando o sistema possível e determinado!

É muito verboso, é muito textual e é necessário algum conhecimento em álgebra linear para o entendimento do raciocínio exposto acima. Entretanto, tudo isso pode ser esquematizado em um simples algoritmo exposto nos próximos slides.

</div>
