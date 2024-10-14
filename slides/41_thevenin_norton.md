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

Pela lei de Ohm sabemos que \\(R = {{V} \over {I}}\\). Se temos uma tensão de Thévenin \\(V_{th}\\) e uma corrente de curtocircuito (Norton) \\(I_{\\text{cc}}\\), podemos obter a resistência de Thévenin \\(R_{th}\\) como:

\\[
R_{th} = {{V_{th}} \over {I_{\\text{cc}}}}
\\]

Se quisermos construir o equivalente de Thévenin, basta construirmos um circuito com uma fonte de tensão \\(V_{th}\\) em série com uma resistência \\(R_{th}\\). Se quisermos construir o equivalente de Norton, basta construirmos um circuito com uma fonte de corrente \\(I_{\\text{cc}}\\) em paralelo com uma resistência \\(R_{th}\\). E assim verificamos o método tradicional.

Por que este método é importante? Porque em ocasiões em que o procedimento algorítimico para obtenção de equivalentes de Thévenin (Norton) resultar em valores inconsistentes (estranhos) temos mais uma ferramenta de verificação para certificar se o resultado está correto ou não.
