# Caminhos em uma Escadaria
## Sugestão de Grafo Pandora
![Representação Visual do Grafo Pandora](grafo_programa_desafio3.png)
> O diagrama para o programa Pandora acima pode ser acessado no arquivo [desafio3.json](./desafio3.json).
>
> Para visualizar o grafo, você pode usar a [IDE Web de Pandora](https://salgado2004.github.io/Pandora-web-IDE). Basta importar o arquivo `desafio3.json` no editor para explorar a estrutura do grafo.

## Explicação
Esse desafio propõe a criação de uma função `quantidadeCaminhos(n)` que retorna a quantidade de formas diferentes de subir uma escadaria com `n` degraus, considerando que em cada movimento é possível subir 1 ou 2 degraus.

A lógica para resolver o problema envolve identificar os subproblemas necessários para calcular a quantidade de caminhos para qualquer degrau `n`. A função deve considerar os casos base:
- Para o degrau 0, existe exatamente 1 maneira de permanecer nele.
- Para o degrau 1, existe exatamente 1 maneira de chegar a ele.
- Para o degrau `n` (n > 1), a quantidade de caminhos é a soma das quantidades de caminhos para os degraus `n-1` e `n-2`, pois o último movimento pode ter sido subir 1 degrau (vindo de `n-1`) ou subir 2 degraus (vindo de `n-2`).

Sendo assim, a função `quantidadeCaminhos(n)` pode ser implementada de forma recursiva, utilizando a relação de recorrência:
```
quantidadeCaminhos(n) = n > 1 ? quantidadeCaminhos(n - 1) + quantidadeCaminhos(n - 2) : 1
```

O grafo Pandora representa as operações de verificação dos casos base (simplificando `n = 0` e `n = 1` como `n < 2`), a chamada recursiva para os degraus `n-1` e `n-2`, e a soma dos resultados dessas chamadas para obter a quantidade total de caminhos para o degrau `n`.

## Resultado esperado do desafio
Espera-se que os participantes sejam capazes de identificar a estrutura recursiva do problema, reconhecendo que a quantidade de caminhos para um determinado degrau pode ser obtida a partir das soluções de subproblemas menores. O desafio busca evidenciar processos de mapeamento estrutural, por meio da compreensão das relações entre os diferentes estados do problema, e de identificação de similaridades, observadas na aplicação recorrente da mesma regra para valores distintos de entrada. 

Espera-se ainda observar evidências de decomposição, associadas à capacidade de representar um problema complexo como a combinação de subproblemas menores e interdependentes, e também de generalização, presente na formulação de uma regra válida para qualquer valor de `n`.