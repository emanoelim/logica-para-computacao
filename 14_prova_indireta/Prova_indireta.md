## Prova indireta / Por contradição / Redução ao absurdo
A partir de uma contradição é possível deduzir qualquer proposição. Considere por exemplo a proposição p ^ ~p. 
Vamos deduzir α a partir dessa contradição:
```diff
1. p ^ ~p   P
_____________
2. p        1 – S
3. ~p       1 – S
4. p v α    2 – A
5. α        4, 3 – SD
```
Isso quer dizer que se a partir de um conjunto de premissas eu conseguir encontrar uma contradição qualquer, 
está provada a validade do argumento.

Para isso introduzimos a negação da conclusão como uma hipótese e deduzimos uma contradição qualquer, pois:

(P ^ ~α) → α ⟺ P → α

Pelo princípio da exportação sabemos que:

(P ^ α) → β ⟺ P → (α → β)

considerando que:

~α = α

α = β

e substituindo na fórmula acima, temos:

(P ^ ~α) → α ⟺ P → (~α → α)

aplicando a Lei da Condicional sobre P → (~α → α):

P → (~(~α) v α)

P → (α v α)

P → α

Portanto, podemos dizer que:

(P ^ ~α) → α ⟺ P → α

Ou seja, provando o argumento do tipo (P ^ ~α) → α, também está provado o argumento P → α.

Para a prova indireta, aplicam-se as mesmas regras para o raciocínio hipotético vistas na prova da condicional.

### Exemplos

1. Provar "~p" a partir de:
```diff
1. p -> q
2. ~q
```
Solução:
```diff
1. p -> q      P
2. ~q          P
________________
3. | p          H
4. | q          1, 3 - MP
5. | ~q ^ q     2, 4 - U
6. ~p           3 - 5 - RAA
```
A hipotese fica vigente até a finalização da prova, ou seja, até encontrar uma contradição.

2. Provar "~(p ^ q)" a partir de:
```diff
1. p <-> ~q
```
Solução:
```diff
1. p <-> ~q                  P
______________________________
2.  | p ^ q                  H
3.  | p                      2 - S
4.  | q                      2 - S
5.  | (p -> ~q) ^ (~q -> p)  1 - Eliminação do bicondicional
6.  | p -> ~q                5 - S
7.  | ~q -> p                5 - s
8.  | ~q                     6, 3 - MP
9.  | ~q ^ q                 8, 4 - U
10. ~(p ^ q)                 2 - 9 - RAA
```

3. Provar “r” a partir de:
```diff
1. ~p → r    
2. ~r → q    
3. ~(p ^ q)    
```

Solução:
```diff
1. ~p → r        P
2. ~r → q        P
3. ~(p ^ q)      P
__________________
4.  | ~r         H
5.  | ~~p        1, 4 - MT
6.  | p          5 - DN
7.  | q          2, 4 - MP
8.  | ~p v ~q    3 - Morgan
9.  | ~p         7, 8 - SD
10. | p ^ ~p     6, 9 - U
11. r            4 - 10 - RAA (Redução ao absurdo)
```

## Referências
- Daghlian, Jacob, **Lógica e Álgebra de Boole**, Atlas, 4ª edição, 2009.
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.

