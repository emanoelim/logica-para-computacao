## Exercícios

1. Verifique a validade dos argumentos utilizando regras de inferência: 

a) p v q, p → r, ~r ⊢ q v s

b) p → (q → r), p → q, p ⊢ r

c) p → s, p ^ q, s ^ r → ~t, q → r ⊢ ~t

d) s ^ q, t → ~q, ~t → r ⊢ r v ~s

e) p v q → (p → s ^ t), p ^ r ⊢ t v u
___
2. Provar ~t dadas as premissas abaixo:
```diff
1. p → s
2. p ^ q
3. s ^ r → ~t
4. q → r
```
___
3. Provar t ^ s dadas as premissas abaixo:
```diff
1. e → s
2. ~t → ~j
3. e ^ j
```
___
4. Provar s dadas as premissas abaixo:
```diff
1. p → (q ^ r)
2. p
3. t → ~q
4. t v s
```
___
5. Considere as seguintes premissas:

- Se o universo é finito, então a vida é curta.
- Se a vida vale a pena, então a vida é complexa.
- Se a vida é curta ou complexa, então a vida tem sentido.
- A vida não tem sentido.

Cada item a seguir é uma conclusão para as premissas acima. Assim, prove a validade de cada argumento formado usando as 
regras de inferência.

a) A vida não é curta.

b) A vida não é complexa ou o universo não é finito.

c) A vida vale a pena se e somente se a vida tem sentido.
