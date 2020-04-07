## Tabelas verdade

Até o momento, o enunciado dos problemas nos fornecia uma fórmula e as interpretações de cada símbolo proposicional da fórmula. A partir 
disso era possível determinar  se a fórmula tinha uma resposta verdadeira ou falsa. Por exemplo: 

E = ~p v r
- I[p] = V
- I[r] = V

| **p** | **r** | **~p** | **~p v r** |
|-------|-------|--------|------------|
| V     | V     | F      | V          |

Futuramente, para determinar se um argumento é válido ou não, vamos precisar testar todas as combinações possíveis de Vs e Fs. No exemplo 
acima, faríamos:

| **p** | **r** | **~p** | **~p v r** |
|-------|-------|--------|------------|
| V     | V     | F      | V          |
| V     | F     | F      | F          |
| F     | V     | V      | V          |
| F     | F     | V      | V          |

Como a fórmula tem apenas 2 símbolos proposicionais, fica fácil determinar todas as combinações possíveis de Vs e Fs. Mas se fosse uma 
fórmula com 3, 4, 5 símbolos proposicionais? 

O número de combinações possíveis de Vs e Fs é dado por 2<sup>n</sup>, onde n é o número de símbolos proposicionais que aparecem na 
fórmula. Se tivermos por exemplo, uma fórmula com 2 símbolos, teremos 2<sup>2</sup> = 4 combinações possíveis. Se tivermos uma fórmula 
com 3 símbolos, teremos 2<sup>3</sup> = 8 combinações possíveis. Se tivermos uma fórmula com 4 símbolos, teremos 2<sup>4</sup> = 16 
combinações possíveis, e assim por diante.

Conforme o número de símbolos cresce, fica difícil lembrar de todas as combinações possíveis, por isso podemos usar a seguinte 
estratégia para facilitar:
- Criamos uma tabela contendo inicialmente uma coluna para cada símbolo proposicional.
- Selecionamos a última coluna e preenchemos com intercalações de Vs e Fs.
- Selecionamos a penúltima coluna e preenchemos com intercalações de 2 Vs e 2 Fs.
- Selecionamos a antepenúltima coluna e preenchemos com intercalações de 4 Vs e 4 Fs.

E assim por diante, sempre dobrando.

Por exemplo:

| **p** | **q** | **r** |
|-------|-------|-------|
| V     | V     | V     |
| V     | V     | F     |
| V     | F     | V     |
| V     | F     | F     |
| F     | V     | V     |
| F     | V     | F     |
| F     | F     | V     |
| F     | F     | F     |

Tendo todas as combinações possíveis, resolvemos cada linha da tabela, levando em conta os parênteses e a ordem de precedência dos
operadores. Por exemplo, a fórmula **(~p ^ q) → (r v p)**:

| **p** | **q** | **r** | **~p** | **~p ^ q** | **r v p**| **(~p ^ q) → (r v p)** |
|-------|-------|-------|--------|------------|----------|------------------------|
| V     | V     | V     | F      | F          | V        | V                      |
| V     | V     | F     | F      | F          | V        | V                      |
| V     | F     | V     | F      | F          | V        | V                      |
| V     | F     | F     | F      | F          | V        | V                      |
| F     | V     | V     | V      | V          | V        | V                      |
| F     | V     | F     | V      | V          | F        | F                      |
| F     | F     | V     | V      | F          | V        | V                      |
| F     | F     | F     | V      | F          | F        | V                      |




