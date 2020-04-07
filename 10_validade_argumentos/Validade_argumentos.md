## Validade de argumentos

Um argumento é formado por um conjunto de proposições, onde P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub>, …, P<sub>n</sub> são premissas e 
Q é a conclusão:

P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub>, …, P<sub>n</sub>  ⟝ Q

Um argumento é válido se e somente se todas as suas interpretações são válidas. Uma interpretação é válida se é impossível que a 
conclusão seja falsa enquanto as premissas são verdadeiras. Um argumento não válido é chamado de **sofisma**.

Considere o argumento: 

A princesa ou a rainha comparecerá a cerimônia.

A princesa não comparecerá.

∴ A rainha comparecerá.

Considerando:
 
p = A princesa comparecerá.

q = A rainha comparecerá.  
        
temos:

p v q, ~p ⟝ q

Para verificar se o argumento é válido vamos construir sua tabela verdade, pois esta possibilita testar todas as suas interpretações.
Vamos adicionar uma coluna para cada premissa e ao final vamos adicionar uma coluna para a conclusão:

| **p** | **q** | **p v q** | **~p** | **q** |
|-------|-------|-----------|--------|-------|
| V     | V     | V         | F      | V     |
| V     | F     | V         | F      | F     |
| F     | V     | V         | V      | V     |
| F     | F     | F         | V      | F     |

Precisamos verificar as linhas onde todas as premissas são verdadeiras. Existe apenas um caso onde isso acontece (linha 3), e a
conclusão também é verdadeira. Ou seja, neste argumento não existe nenhuma interpretação onde premissas verdadeiras levam a uma 
conclusão falsa. Logo, ele é válido.

Já o argumento abaixo formalizado:

p -> q, q ⟝ p

é inválido. Ou seja, um sofisma. Pois ao construir sua tabela verdade:

| **p** | **q** | **p -> q** | **q** | **p** |
|-------|-------|------------|-------|-------|
| V     | V     | V          | V     | V     |
| V     | F     | F          | F     | V     |
| F     | V     | V          | V     | F     |
| F     | F     | V          | F     | F     |

Verificamos que existem dois casos onde as duas premissas são verdadeiras (linahs 1 e 3). Na linha 1, a conclusão também é verdadeira. 
Na linha 3, a conclusão é falsa, o que torna o argumento inválido, uma vez que premissas verdadeiras não podem levar a uma conslusão 
falsa.

### Validade de argumento e implicação lógica

Quando todas as premissas são verdadeiras, o resultado da conjunção dessas premissas também é verdadeiro. Para faciltar a analise do argumento, podemos criar na tabela uma coluna com o resultado da conjunção de todas as premissas, seguida pela coluna da conclusão. Desta forma, em vez de procurar uma sequência de Vs seguidas de um F, basta procurar a combinação V - F. Considerando o exemplo p -> q, q ⟝ p:

| **p** | **q** | **p -> q** | **q** | **(p -> q) ^ q** | **p** |
|-------|-------|------------|-------|------------------|-------|
| V     | V     | V          | V     | V                | V     |
| V     | F     | F          | F     | F                | V     |
| F     | V     | V          | V     | V                | F     |
| F     | F     | V          | F     | F                | F     |

Verificamos que a combinação V - F aparece na linha 3. O argumento não é válido. 

Buscamos por este mesmo padrão quando queremos testar se uma fórmula implica logicamente em outra. Ou seja, podemos dizer que quando um argumento é válido, **a conjunção das premissas implica logicamente na conclusão**.

### Validade de argumento e tautologia

Anteriormente vimos que se P implica logicamente em Q, a tabela verdade de P -> Q deve ser uma tautologia. Assim, outra forma de verificar se um argumento é válido, é construir a tabela de:

P<sub>1</sub> ^ P<sub>2</sub> ^ P<sub>3</sub> ^ … ^ P<sub>n</sub> -> Q

e verificar se o resultado é uma tautologia.

Considerando o exemplo anterior, basta adicionar na tabela uma coluna com o resultado de ((p -> q) ^ q) -> p. Se o resultado for uma
tautologia, então o argumento é válido.

| **p** | **q** | **p -> q** | **q** | **(p -> q) ^ q** | **p** | **((p -> q) ^ q) -> p** |
|-------|-------|------------|-------|------------------|-------|-------------------------|
| V     | V     | V          | V     | V                | V     | V                       |
| V     | F     | F          | F     | F                | V     | V                       |
| F     | V     | V          | V     | V                | F     | F                       |
| F     | F     | V          | F     | F                | F     | V                       |

Como o resultado da implicação das premissas na conclusão não é uma tautologia, então o argumento não é válido.

Já no exemplo p v q, ~p ⟝ q, teremos a seguinte tabela:

| **p** | **q** | **p v q** | **~p** | **(p v q) ^ ~p** | **((p v q) ^ ~p) -> q** |
|-------|-------|-----------|--------|------------------|-------------------------|
| V     | V     | V         | F      | F                | V                       |
| V     | F     | V         | F      | F                | V                       |
| F     | V     | V         | V      | V                | V                       |
| F     | F     | F         | V      | F                | V                       |

O resultado da implicação das premissas na conclusão é uma tautologia, então o argumento é válido.

## Referências
- Daghlian, Jacob. **Lógica e Álgebra de Boole**. Editora Atlas. 4ª edição. 2009.


