## Prova da condicional
Suponha que você precisa provar α → β a partir de um conjunto de premissas P (P<sub>1</sub>, P<sub>2</sub> … P<sub>n</sub>), 
ou seja: P → (α → β) deve ser uma tautologia.

#### Princípio da exportação
O princípio da exportação diz que:

P → (α → β) ⟺ (P ^ α) → β

O princípio é demonstrado a partir da Lei da Condicional (ver arquivo sobre equivalências lógicas), que diz que:

a → b ⟺ ~a v b

Considerando:

P = a

(α → β) = b

aplicando a Lei da Condicional em P → (α → β), temos:

~P v (α → β)

Aplicando novamente a Lei da Condicional dentro dos parênteses temos:

~P v (~α v β)

que pelas Leis Associativas pode ser reescrito como:

(~P v ~α) v β

aplicando a Lei de Morgan a fórmula pode ser reescrita:

~(P v α) v β

e por fim, considerando que:

P v α = a

β = b

pela Lei da Condicional tem-se:

(P v α) → β

Portanto, podemos dizer que:

P → (α → β) ⟺ (P ^ α) → β

Sendo assim, se (P ^ α) → β é uma tautologia, então a proposição equivalente P → (α → β) também é, ou seja, é possível deduzir 
α → β a partir de P. Assim, para provar um argumento onde a conclusão tem a forma α → β, basta introduzir o antecendente α 
como uma hipótese (ou premissa provisória) e deduzir o consequente β.

### Exemplos

1. Provar r → ~p a partir de:
```diff
1. p → q
2. r → ~q
```
Devemos introduzir a hipótese “r” para achar “~p”:
```diff
1. p → q       P
2. r → ~q      P
________________
3. | r         H
4. | ~q        2, 3 - MP
5. | ~p        1, 4 - MT
6. r → ~p      3 - 5 - PC (Prova da Condicional)
```

Ao adicionarmos a hipótese, iniciamos uma linha vertical para indicar a duração do argumento hipotético. Essa linha continua
até a hipótese ser descartada pela aplicação da PC (até achar o consequente).

2. Provar c → ~d, a partir de:
```diff
1. b → ~c
2. ~(d ^ ~b)
```
Devemos introduzir a hipótese “c”, para achar “~d”:
```diff
1. b → ~c          P
2. ~(d ^ ~b)       P
____________________
3. | c             H
4. | ~~c           3 - DN
5. | ~b            1, 4 - MT
6. | ~d v ~~b      2 - Morgan
7. | ~d v b        6 - DN
8. | ~d            7, 5 - SD
9. c → ~d          3 - 8 - PC
```
3. Provar (p -> q) -> q a partir de:
```diff
1. p
```
Devemos introduzir a hipótese “(p -> q)”, para achar “q”:
```diff
1. p               P
____________________
2. | p -> q        H
3. | q             2, 1 - MP
4. (p -> q) -> q   2 - 3 - PC 
```
Ocasionalmente, conclusões que são condicionais tem consequentes que são condicionais, como no exemplo 4:

4. (p ^ q) -> r ├ p -> (q -> r)

Nesse caso a mesma estratégia é adotada, adicionamos p como hipótese e então tentamos encontrar q -> r. Sendo o consequente 
q -> r um condicional, pode-se usar a mesma abordagem e colocar q como uma hipótese e então encontrar r:
```diff
1. (p ^ q) -> r      P
______________________
2. | p               H
3. | | q             H
4. | | p ^ q         2, 3 - U
5. | | r             1, 4 - MP
6. | q -> r          3 - 5 - PC
7. p -> (q -> r)     2, 6 - PC
```

### Regras para o raciocínio hipotético
Quando usamos o raciocínio hipotético, várias regras devem ser seguidas:

 1. Cada hipótese introduz numa prova o início de uma nova linha vertical. Essa linha continua até a hipótese ser descartada
 pela aplicação da PC.
 
 2. Nenhuma fórmula do lado direito da linha vertical pode ser citada após o término da linha vertical.
 
 3. Se duas ou mais hipóteses são vigentes simultaneamente, a ordem na qual são descartadas deve ser a ordem inversa na qual 
 foram introduzidas (assimo como foi feito no exemplo 4).
 
 4. Uma prova não está completa até que todas as hipóteses sejam descartadas.
 
 ## Prova da bicondicional
A prova de um argumento cuja conclusão tem a forma α ↔ β é feita de maneira semelhante a prova da condicional, só que em duas etapas:

1ª - Provamos α → β

2ª - Provamos β → α

Pois, se temos α → β e β → α, pela lei da introdução da bicondicional (Ibic) temos α ↔ β.

1. Provar a ↔ u a partir de:
```diff
1. t → a
2. u → t
3. a → m
4. u v ~m
```
1º passo: provar a → u
```diff
1. t → a        P
2. u → t        P
3. a → m        P
4. u v ~m       P
_________________
5. | a          H
6. | m          3, 5 - MP
7. | ~~m        6 - DN
8. | u          4, 7 - SD
9. a → u        5 - 8 - PC
```
2º passo: provar u → a
```diff
1. t → a         P
2. u → t         P
3. a → m         P 
4. u v ~m        P
__________________
5. | u           H
6. | t           2, 5 - MP
7. | a           1, 6 - MP
8. u → a         5 - 7 - PC
```

 ## Referências
- Daghlian, Jacob., **Lógica e Álgebra de Boole**, Atlas, 4ª edição, 2009.
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.


