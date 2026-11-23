# Separação em Duas Listas
## Sugestão de Grafo Pandora
![Representação Visual do Grafo Pandora](grafo_programa_desafio8.png)
> O diagrama para o programa Pandora acima pode ser acessado no arquivo [desafio8.json](./desafio8.json).
>
> Para visualizar o grafo, você pode usar a [IDE Web de Pandora](https://salgado2004.github.io/Pandora-web-IDE). Basta importar o arquivo `desafio8.json` no editor para explorar a estrutura do grafo.

## Explicação
O desafio 8 é uma continuação do desafio 7, mas com uma abordagem que envolve a separação de elementos em duas listas distintas com base em um critério definido. A função `separar(lista, teste)` é projetada para percorrer uma lista e aplicar um critério de seleção definido pela função `teste`. Essa função `teste` recebe um elemento da lista e retorna verdadeiro ou falso, determinando se o elemento deve ser incluído na primeira lista ou na segunda.

A principal diferença em relação ao desafio anterior é que, em vez de criar uma única lista filtrada, agora estamos criando duas listas: uma contendo os elementos que atendem ao critério definido pela função `teste` e outra contendo os elementos que não atendem a esse critério.

Para lidar com essa estrutura adicional, sem tornar a função `separar` muito complexa, podemos utilizar uma função `auxiliar(listaExterna, resultado, elemento)` que encapsula a lógica de separação, permitindo que a função principal permaneça clara e concisa. No grafo Pandora acima, a função `separar` é responsável por percorrer a lista até o final, aplicando a função `teste` a cada elemento e delegando a decisão de inclusão para a função `auxiliar`. A função `auxiliar` então decide se o elemento deve ser adicionado à primeira lista ou à segunda, com base no resultado da função `teste`, retornando as duas listas resultantes encapsuladas em uma lista externa.

Os exemplos utilizados permanecem os mesmos do desafio anterior, como números pares e números maiores que 10, conforme os exemplos abaixo:
![Grafo Pandora com Função Main executando separar com ehPar](./grafo_main_ehPar.png)

![Grafo Pandora com Função Main executando separar com maiorQue10](./grafo_main_ehMaiorQue10.png)
Em ambos os casos, a função `separar` é chamada com a lista de entrada e a função de teste correspondente, resultando em duas novas listas: uma contendo os elementos que atendem ao critério definido e outra contendo os elementos que não atendem.

## Resultado esperado do desafio
Como desafio final da sequência, espera-se que os participantes sejam capazes de reutilizar e expandir abstrações construídas anteriormente para resolver um problema estruturalmente mais complexo.  desafio busca evidenciar processos de reutilização e composição funcional, observados na combinação entre mecanismos de percurso, critérios de classificação e estruturas auxiliares para construção do resultado. 

Espera-se ainda observar evidências de mapeamento estrutural e identificação de similaridades, uma vez que a solução exige reconhecer padrões já presentes no desafio de filtragem e adaptá-los para produzir simultaneamente duas coleções relacionadas. A utilização de funções de ordem superior e de estruturas compostas oferece uma oportunidade para observar formas mais avançadas de abstração e modularidade durante a resolução de problemas.