# Padrões em uma Sequência de Resultados
## Sugestão de Grafo Pandora
![Representação Visual do Grafo Pandora](grafo_programa_desafio1.png)
> O diagrama para o programa Pandora acima pode ser acessado no arquivo [desafio1.json](./desafio1.json).
>
> Para visualizar o grafo, você pode usar a [IDE Web de Pandora](https://salgado2004.github.io/Pandora-web-IDE). Basta importar o arquivo `desafio1.json` no editor para explorar a estrutura do grafo.

## Explicação
A lógica do programa Pandora para o desafio 1 é baseada na análise da sequência de resultados favoráveis (V) e desfavoráveis (D) ao longo dos dias. A tabela de resultados mostra um padrão alternado, onde os dias ímpares apresentam resultados desfavoráveis (D) e os dias pares apresentam resultados favoráveis (V).

Sendo assim, a função `resultado(n)` pode ser definida da seguinte forma:
- Se `n` for ímpar, o resultado será "D" (desfavorável).
- Se `n` for par, o resultado será "V" (favorável).

A expressão da função é definida por `resultado(n) = "V" se n % 2 == 0, caso contrário "D"`.

No grafo Pandora, os valores `2`, `0`, `D` e `V` são representados como constantes, enquanto a operação de módulo (`%`) é representada como uma operação de nó. A decisão final sobre o resultado é feita com base na avaliação da condição `n % 2 == 0`, que determina se o dia é par ou ímpar.

## Resultado esperado do desafio
Espera-se que os participantes sejam capazes de identificar o padrão presente nos exemplos fornecidos e construir uma regra geral capaz de prever resultados para valores não observados anteriormente. Espera-se observar evidências de filtragem de informações, por meio da distinção entre dados relevantes e irrelevantes do enunciado, e de identificação de similaridades, por meio do reconhecimento da alternância entre posições pares e ímpares. A formulação de uma função capaz de representar o comportamento para qualquer valor positivo de entrada constitui uma evidência adicional de generalização e abstração da regularidade observada.