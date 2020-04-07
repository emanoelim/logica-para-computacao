## Operações lógicas
Como visto anteriormete, uma proposição está associada a um valor lógico: verdadeiro ou falso (V ou F).  Exemplos:
- p = O Japão fica na África.
- q = O Brasil ganhou a copa de 1970 no México.

A proposição p é falsa, portanto recebe o valor lógico F. 

A proposição q é verdadeira, portanto recebe o valor lógico V.

Também vimos que elas seguem dois princípios:
- **Princípio da não contradição:** uma proposição não pode ser simultaneamente verdadeira e falsa.
- **Princípio do terceiro excluído:** toda proposição é somente verdadeira ou somente falsa, nunca ocorrendo um terceiro caso.

Suponha agora, que você tem a seguinte fórmula da lógica proposicional:
- p ^ ~q
onde p = V e q = F. O resultado da fórmula será V ou F?

Para ter essa resposta precisamos compreender o efeito de cada um dos operadores lógicos estudados anteriormente:
- Negação (~)
- Conjunção (^)
- Disjunção (v)
- Condicional (→)
- Bicondicional (↔)

### Negação (~)
O operador de negação tem a característica de inverter o valor de uma proposição. 

Seja p uma proposição. A negação de uma proposição p é definida pela tabela abaixo:

| **p** | **~p** |
|---|----|
| V | F  |
| F | V  |

Se a proposição p significar "o Sol é uma estrela" e tiver valor verdadeiro, ~p (o Sol não é uma estrela), terá valor falso.

Se a proposição p significar: "Roma é a capital da França" e tiver valor falso, ~p (Roma não é a capital da França), terá valor verdadeiro.

### Conjunção (^)
Sejam p e q duas proposições. Existem quatro combinações possíveis de p e q considerando os valores V e F. A conjunção das proposições 
p e q é definida pela tabela abaixo:

| **p** | **q** | **p ^ q** |
|---|---|-------|
| V | V | V     |
| V | F | F     |
| F | V | F     |
| F | F | F     |

O resultado da conjunção será verdadeiro somente quando todas as proposições tiverem valor verdadeiro.

Se considerarmos que:
- p = Eu tenho uma laranja. (V)
- q = Eu tenho uma maçã. (V)

Ao afirmar p ^ q estou contando a verdade: eu afirmei que tinha as duas frutas, e eu realmente tinha.

Se consideramos que:
- p = Eu tenho uma laranja. (V)
- q = Eu tenho uma maçã. (F)

Ao afirmar p ^ q estou contando uma mentira: eu afirmei que tinha as duas frutas, mas tinha somente a laranja.

Se consideramos que:
- p = Eu tenho uma laranja. (F)
- q = Eu tenho uma maçã. (V)

Ao afirmar p ^ q estou contando uma mentira: eu afirmei que tinha as duas frutas, mas tinha somente a maçã.

Se consideramos que:
- p = Eu tenho uma laranja. (F)
- q = Eu tenho uma maçã. (F)

Ao afirmar p ^ q estou contando uma mentira: eu afirmei que tinha as duas frutas, mas não tinha fruta alguma.

### Disnjunção (^)
Sejam p e q duas proposições. Existem quatro combinações possíveis de p e q considerando os valores V e F. A conjunção das proposições 
p e q é definida pela tabela abaixo:
| **p** | **q** | **p v q** |
|---|---|-------|
| V | V | V     |
| V | F | V     |
| F | V | V     |
| F | F | F     |

O resultado da disjunção será verdadeiro sempre que houver ao menos uma proposição verdadeira.

Se consideramos que:
- p = Eu tenho uma laranja. (V)
- q = Eu tenho uma maçã. (V)

Ao afirmar p v q estou contando uma verdade: eu afirmei que tinha ao menos uma das duas frutas, e realmente tinha.

Se consideramos que:
- p = Eu tenho uma laranja. (V)
- q = Eu tenho uma maçã. (F)

Ao afirmar p v q ainda estou contando uma verdade: eu afirmei que tinha ao menos uma das duas frutas, e realmente tinha.

Se consideramos que:
- p = Eu tenho uma laranja. (F)
- q = Eu tenho uma maçã. (V)

Ao afirmar p v q ainda estou contando uma verdade: eu afirmei que tinha ao menos uma das duas frutas, e realmente tinha.

Se consideramos que:
- p = Eu tenho uma laranja. (F)
- q = Eu tenho uma maçã. (F)

Ao afirmar p v q estou contando uma mentira: eu afirmei que tinha ao menos uma das duas frutas, quando não tinha nenhuma.

### Condicional (→)
Sejam p e q duas proposições. A implicação de p em q é definida pela tabela:
| **p** | **q** | **p → q** |
|---|---|-------|
| V | V | V     |
| V | F | F     |
| F | V | V     |
| F | F | V     |

O resultado é falso somente quando algo verdadeiro implica em algo falso.

A tabela de p → q é obtida como é mostrado abaixo. Considere a proposição:
- “Se Paula vai à festa, então Maria vai à festa”.

Esta proposição tem o mesmo significado de:

“Não é o verdade que Paula vai à festa e Maria não vai à festa”.

Considerando que:
- p = Paula vai à festa.
- q = Maria vai à festa.

"Se Paula vai à festa, então Maria vai à festa”. É formalizado como: p → q

“Não é verdade que Paula vai à festa e Maria não vai à festa”. É formalizado como: ~(p ^ ~q) 

Esta é uma wff mais complexa. Para montar a sua tabela devemos resolve-la por partes. Como na matemática, vamos resolver primeiro o que está entre parênteses, que é p ^ ~q. Como veremos adiante, o operador de negação tem prioridade em relação ao operador de conjunção. Então devemos resolver ~q e depois obter o resultado de p ^ ~q. Por fim, aplicamos a negação ao resultado desta conjunção e temos o resultado final de ~(p ^ ~q).
| **p** | **q** | **~q** | **p ^ ~q** | **~(p ^ ~q)** |
|-------|-------|--------|------------|---------------|
| V     | V     | F      | F          | V             |
| V     | F     | V      | V          | F             |
| F     | V     | F      | F          | V             |
| F     | F     | V      | F          | V             |

A última coluna tem exatamente os mesmos valores da tabela da implicação.

### Bicondicional (↔)
Sejam p e q duas proposições. A bi implicação de p em q é definida pela tabela:
| **p** | **q** | **p ↔ q** |
|---|---|-------|
| V | V | V     |
| V | F | F     |
| F | V | F     |
| F | F | V     |

Podemos ver que p ↔ q é verdadeira somente quando antecedente e consequente tem o mesmo valor lógico.

Considere o exemplo: “T é um triângulo, se e somente se, T é um polígono de 3 lados.”

Como visto anteriormente, isso é o mesmo que dizer que: “Se T é um triângulo, então T é um polígono de 3 lados” e “Se T é um polígono de 3 lados, então T é um triângulo.”.

Sendo assim, a tabela do bicondicional pode ser obtida a partir da conjunção desses dois condicionais:
| **p** | **q** | **p → q** | **q → p** | **(p → q) ^ (q → p)** |
|---|---|---|---|---|
| V | V | V | V | V |
| V | F | F | V | F |
| F | V | V | F | F | 
| F | F | V | V | V |

A última coluna tem exatamente os mesmos valores da tabela da bi-implicação.

## Precedência dos operadores lógicos
Assim como na matemática, os operadores lógicos têm uma ordem de precedência:
1. negação (~)
2. conjunção (^)
3. disjunção (v)
4. condicional (→)
5. bicondicional (↔)

Lembrando que se a fórmula tiver parênteses, devemos resolver primeiro o que está entre parênteses.

## Interpretação de fórmulas
Seja E uma fórmula da lógica proposicional, composta pelas proposições “p”, “q” e “r”.  Para resolver E precisamos saber os valores lógicos de “p”, “q” e “r”. Ou seja, precisamos saber as suas interpretações. A interpretação de “p”, por exemplo, é representada por I[p]. I[p] pode assumir o valor V ou F: I[p] = V ou I[p] = F

**Exemplo 1:**
E = (~p ^ q) → (r v p)
- I[p] = V
- I[q] = F
- I[r] = V

Para descobrir o valor lógico de E, construímos uma tabela iniciando com colunas para os símbolos proposicionais p, q e r. Abaixo de cada símbolo colocamos a sua interpretação:

| **p** | **q** | **r** | 
|---|---|---|
| V | F | V | 

Depois disso, cada parte da fórmula vai sendo resolvida, respeitando a ordem de precedência dos operadores, até chegar no resultado final:
- Primeiro resolvemos a negação:

| **p** | **q** | **r** | **~p** | 
|---|---|---|---|
| V | F | V | F |

- Depois podemos resolver a primeira proposição entre parênteses, ~p ^ q:

| **p** | **q** | **r** | **~p** | **~p ^ q** |
|---|---|---|---|---|
| V | F | V | F | F | 

- Resolvemos então a segunda proposição entre parênteses, r v p:

| **p** | **q** | **r** | **~p** | **~p ^ q** | **r v p**|
|---|---|---|---|---|---|
| V | F | V | F | F | V |

- Agora realizamos a conjunção entre as duas para obter o resultado final:


| **p** | **q** | **r** | **~p** | **~p ^ q** | **r v p**| **(~p ^ q) → (r v p)** |
|---|---|---|---|---|---|---|
| V | F | V | F | F | V | V |

## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.








