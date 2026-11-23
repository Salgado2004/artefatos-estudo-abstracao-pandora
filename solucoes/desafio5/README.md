# Generalização de Potências
## Sugestão de Grafo Pandora
![Representação Visual do Grafo Pandora](grafo_programa_desafio5.png)
> O diagrama para o programa Pandora acima pode ser acessado no arquivo [desafio5.json](./desafio5.json).
>
> Para visualizar o grafo, você pode usar a [IDE Web de Pandora](https://salgado2004.github.io/Pandora-web-IDE). Basta importar o arquivo `desafio5.json` no editor para explorar a estrutura do grafo.

## Explicação
A partir da função `ehPotenciaDeDois(n)` do desafio anterior, a função `ehPotencia(n, base)` generaliza a verificação para qualquer base maior ou igual a 2. A lógica permanece semelhante, mas agora a função precisa lidar com diferentes bases.

Para isso, é necessário primeiro isolar o que era específico para a base 2 e o que permanece igual para qualquer base:
- **O que era específico para a base 2**: 
    - A verificação de paridade e a divisão por 2.
- **O que permanece igual para qualquer base**:
    - A verificação do caso base `n = 1`, que é uma potência de qualquer base.
    - A divisão repetida do número `n` pela base até que o resultado seja 1 ou um número menor que a base.
    - A verificação de divisibilidade de `n` pela base.

Sendo assim, a função `ehPotencia(n, base)` segue a mesma lógica anterior, substituindo os valores que antes eram constantes = `2` pelo parâmetro `base`. A função auxiliar `ehParPositivo(n)` pode ser adaptada para verificar se `n` é divisível pela base, tornando-se `ehDivisor(n, base)`.

## Resultado esperado do desafio
Espera-se que os participantes sejam capazes de analisar criticamente a solução desenvolvida no desafio anterior, identificando quais elementos são específicos da base dois e quais representam aspectos gerais do problema. O desafio busca evidenciar processos de identificação de similaridades, observados no reconhecimento da estrutura comum entre diferentes casos do problema, e de generalização, expressos pela transformação de uma solução específica em uma função parametrizada. 

Além disso, espera-se observar evidências de mapeamento estrutural e reutilização, uma vez que a solução generalizada deve preservar a lógica fundamental construída anteriormente, modificando apenas os elementos necessários para ampliar seu domínio de aplicação.