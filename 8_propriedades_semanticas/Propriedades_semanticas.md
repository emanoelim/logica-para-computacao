## Propriedades semânticas

Durante a construção das tabelas verdade das fórmulas, algumas tabelas apresentam a última coluna toda verdadeira. Outras contém 
linhas verdadeiras e falsas, etc. Vamos analisar cada um dos casos possíveis.

### Tautologia
É toda proposição composta P(p, q, r, …) cujo valor lógico é sempre verdadeiro, quaisquer que sejam os valores lógicos das proposições 
simples que a compõe. Ou seja, chama-se tautologia toda proposição composta cuja última coluna da tabela verdade contém somente Vs. 
Exemplos: 

p v ~(p ^ q)

| **p** | **q** | **p ^ q** | **~(p ^ q)** | **p v ~(p ^ q)** |
|-------|-------|-----------|--------------|------------------|
| V     | V     | V         | F            | V                |
| V     | F     | F         | V            | V                |
| F     | V     | F         | V            | V                |
| F     | F     | F         | V            | V                |

p ^ q -> (p <-> q)

| **p** | **q** | **p <-> q** | **p ^ q**    | **p ^ q -> (p <-> q)** |
|-------|-------|-------------|--------------|------------------------|
| V     | V     | V           | V            | V                      |
| V     | F     | F           | F            | V                      |
| F     | V     | F           | F            | V                      |
| F     | F     | V           | F            | V                      | 

### Contradição
É toda proposição composta P(p, q, r, …) cujo valor lógico é sempre falso, quaisquer que sejam os valores lógicos das proposições simples 
que a compõe. Ou seja, chama-se contradição toda proposição composta cuja última coluna da tabela verdade contém somente Fs. Exemplos:

(p ^ q) ^ ~(p v q)

| **p** | **q** | **p ^ q** | **p v q** | **~(p v q)** | **(p ^ q) ^ ~(p v q)** |
|-------|-------|-----------|-----------|--------------|------------------------|
| V     | V     | V         | V         | F            | F                      |
| V     | F     | F         | V         | F            | F                      |
| F     | V     | F         | V         | F            | F                      |
| F     | F     | F         | F         | V            | F                      |

### Contingência
É toda proposição composta P(p, q, r, …) que não é tautologia e nem contradição. Ou seja, chama-se contingência toda proposição 
composta cuja última coluna da tabela verdade contém ao menos um V e ao menos um F. Exemplo:

p -> ~p

| **p** | **~p** | **p -> ~p** |
|-------|--------|-------------|
| V     | F      | F           |
| F     | V      | V           |

(p v q) -> p

| **p** | **q** | **p v q** | **(p v q)** -> p |
|-------|-------|-----------|------------------|
| V     | V     | V         | V                |
| V     | F     | V         | V                |
| F     | V     | V         | F                |
| F     | F     | F         | F                |

### Satisfatibilidade
Dizemos que uma proposição composta é satisfatível se existe ao menos uma interpretação onde o resultado da proposição é verdadeiro. 
Exemplos:

~p v q

| **p** | **q** | **~p** | **~p v q** |
|-------|-------|--------|------------|
| V     | V     | F      | V          | 
| V     | F     | F      | F          |
| F     | V     | V      | V          | 
| F     | F     | V      | V          | 

Existem 3 interpretações que levam a um resultado verdadeiro, então a fórmula ~p v q é satisfatível.

(p v q) ^ (~p ^ q)

| **p** | **q** | **p v q** | **~p** | **~p ^ q** | **(p v q) ^ (~p ^ q)** |
|-------|-------|-----------|--------|------------|------------------------|
| V     | V     | V         | F      | F          | F                      |
| V     | F     | V         | F      | F          | F                      |
| F     | V     | V         | V      | V          | V                      | 
| F     | F     | F         | V      | F          | F                      |

Existe 1 interpretaçãos que leva a um resultado verdadeiro, então a fórmula (p v q) ^ (~p ^ q) é satisfatível.

- **Satisfatibilidade e tautologia:** se uma fórmula é uma tautologia, ela é satisfatível.
- **Satisfatibilidade e contingência:** se uma fórmula é uma contingência, ela é satisfatível.
- **Satisfatibilidade e contradição:** se uma fórmula é uma contradição, ela não é satisfatível.

### Equivalência lógica
Duas proposições são equivalentes quando o resultado de suas tabelas verdade é idêntico. A equivalência lógica geralmente é denotada pelo símbolo ⟺. Exemplos:

p ⟺ ~~p

| **p** | **~p** | **~~p** |
|-------|--------|---------|
| **V** | F      | **V**   |
| **F** | V      | **F**   |

~(p v q) ⟺ ~p ^ ~q

| **p** | **q** | **p v q** | **~(p v q)** | **~p** | **~q** | **~p ^ ~q** |
|-------|-------|-----------|--------------|--------|--------|-------------|
| V     | V     | V         | **F**        | F      | F      | **F**       |
| V     | F     | V         | **F**        | F      | V      | **F**       |
| F     | V     | V         | **F**        | V      | F      | **F**       |
| F     | F     | F         | **V**        | V      | V      | **V**       |

- **Equivalência lógica e tautologia:** sempre que as proposições compostas P e Q forem equivalentes, então a tabela de P <-> Q deve 
ser uma tautologia.
Considerando o exemplo acima, se ~(p v q) ⟺ ~p ^ ~q, então a tabela de ~(p v q) <-> (~p ^ ~q) é tautologia:

| **p** | **q** | **p v q** | **~(p v q)** | **~p** | **~q** | **~p ^ ~q** | **~(p v q) <-> ~p ^ ~q** |
|-------|-------|-----------|--------------|--------|--------|-------------|--------------------------|
| V     | V     | V         | F            | F      | F      | F           | V                        |
| V     | F     | V         | F            | F      | V      | F           | V                        |
| F     | V     | V         | F            | V      | F      | F           | V                        |
| F     | F     | F         | V            | V      | V      | V           | V                        |

### Implicação lógica
Se construirmos a tabela verdade de uma proposição P e a tabela verdade de uma proposição Q, compararmos a última coluna de cada tabela e não formos capazes de identificar alguma linha onde P é V e Q é F, então podemos dizer que P implica logicamente em Q. A implicação
lógica é denota pelo símbolo ⟹.

p ^ q ⟹ p v q?

| **p** | **q** | **p ^ q** | **p v q** |
|-------|-------|-----------|-----------|
| V     | V     | **V**     | **V**     |
| V     | F     | **F**     | **V**     |
| F     | V     | **F**     | **V**     |
| F     | F     | **F**     | **F**     |

Não existe nenhuma linha onde ocorre V e F, então **podemos dizer que p ^ q implica logicamente em p v p**.

 p v q ⟹ p ^ q?
 
| **p** | **q** | **p v q** | **p ^ q** |
|-------|-------|-----------|-----------|
| V     | V     | **V**     | **V**     |
| V     | F     | **V**     | **F**     | 
| F     | V     | **V**     | **F**     | 
| F     | F     | **F**     | **F**     |

Existem duas linhas onde ocorre V e F, então **não podemos dizer que p v q implica logicamente em p ^ q**.

- **Implicação lógica e tautologia:** Se P implica logicamente em Q, então a tabela de P -> Q deve ser tautologia. Considerando o exemplo de p ^ q ⟹ p v q:

| **p** | **q** | **p ^ q** | **p v q** | **p ^ q -> p v q** |
|-------|-------|-----------|-----------|--------------------|
| V     | V     | **V**     | **V**     | **V**              |
| V     | F     | **F**     | **V**     | **V**              |
| F     | V     | **F**     | **V**     | **V**              |
| F     | F     | **F**     | **F**     | **V**              |

## Referências
- João Nunes de Souza, **Lógica para ciência da computação e áreas afins**, 3<sup>a</sup> ed., GEN LTC, 2014.
