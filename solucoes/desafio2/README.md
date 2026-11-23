# Contagem Recursiva de Elementos
## Sugestão de Grafo Pandora
![Representação Visual do Grafo Pandora](grafo_programa_desafio2.png)
> O diagrama para o programa Pandora acima pode ser acessado no arquivo [desafio2.json](./desafio2.json).
>
> Para visualizar o grafo, você pode usar a [IDE Web de Pandora](https://salgado2004.github.io/Pandora-web-IDE). Basta importar o arquivo `desafio2.json` no editor para explorar a estrutura do grafo.

## Explicação
O desafio 2 propõe a criação de uma função `contarElementos(lista)` que retorna a quantidade de elementos em uma lista, utilizando uma abordagem recursiva. A função deve ser capaz de lidar com listas vazias e listas com qualquer quantidade de elementos, sem receber previamente essa quantidade.

O caso base da recursão ocorre quando a lista está vazia, retornando 0. Para listas não vazias, a função deve contar o primeiro elemento e chamar a si mesma com o restante da lista, somando 1 ao resultado da chamada recursiva.

Os nós do grafo Pandora representam as operações de verificação da lista vazia, a separação do restante da lista com `tail` e a soma do resultado da chamada recursiva com a constante 1, que representa a contagem do primeiro elemento. Para qualquer lista, a função percorre todos os elementos, aplicando a mesma lógica recursiva até atingir o caso base, e então retorna a contagem total de elementos.

## Resultado esperado do desafio
Espera-se que os participantes sejam capazes de representar a estrutura da lista por meio de casos base e casos recursivos, decompondo o problema original em versões progressivamente menores de si mesmo. O desafio busca evidenciar processos de mapeamento estrutural, por meio da identificação das relações entre a lista, seus elementos e o restante da estrutura, assim como processos de identificação de similaridades, observados na aplicação recorrente da mesma estratégia de resolução. Adicionalmente, espera-se observar evidências de decomposição de problemas, uma vez que a solução depende da transformação de uma tarefa complexa em subproblemas estruturalmente equivalentes e mais simples.