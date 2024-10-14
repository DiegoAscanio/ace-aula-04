<style scoped>
    p {
        font-size: 14pt;
    }
    figcaption {
        font-size: 10pt;
    }
    figure {
        margin-left: auto;
        margin-right: auto;
    }
    img {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 315px;
    }
</style>

<!-- _class: lead -->
## Método Tradicional para Obtenção de Equivalentes de Thévenin e Norton

Ainda de acordo com a bibliografia padrão, ao retirar um elemento de um circuito para construir seu equivalente de Thévenin ou Norton, quando aplica-se um curtocircuito entre os terminais \\(A\\) e \\(B\\) do elemento removido, a corrente que flui entre os terminais \\(A\\) e \\(B\\) é a corrente de curto-circuito de Thévenin ou a corrente de Norton - \\(I_{\text{cc}}\\).

<figure>

<!-- _class: transparent -->
![](https://i.imgur.com/tUwi83Q.png)

<figcaption>

Figura 4.4 - Curto circuito entre os terminais \\(A\\) e \\(B\\) de um circuito.

</figcaption>

</figure>

Portanto, se resolvermos o circuito com quaisquer técnicas de análise de circuitos — Leis de Kirchoff das Correntes nos Nós, das Tensões nas Malhas, Lei de Ohm, Método das Tensões nos Nós ou Método das Correntes de Malha — para encontrar a corrente de curtocircuito que passa no curtocircuito adicionado aos terminais \\(A\\) e \\(B\\), teremos a corrente de curtocircuito \\(I_{\text{cc}}\\).
