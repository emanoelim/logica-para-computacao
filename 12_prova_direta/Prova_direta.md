
## Prova direta
Até o momento verificamos que argumentos eram válidos por meio de tabelas verdade. Existem outras formas de verificar a 
validade de um argumento. Uma dessas formas é por meio da prova direta ou derivação. Dado um argumento 

P<sub>1</sub>, P<sub>2</sub>, ..., P<sub>n</sub> ├ Q

este método consiste em deduzir a conclusão Q a partir das premissas P<sub>1</sub>, P<sub>2</sub>, ..., P<sub>n</sub> mediante o uso das regras de inferência 
estudadas anteriormente.

### Exemplos
1. Verificar que o argumento p → ~q, p v ~q, q ├ ~p é válido.
```diff
1) p → ~q    P 
2) p v ~q    P
3) q         P
______________
4) ~~q       3 - DN
5) ~p        1, 4 - MT
```
Inicialmente escrevemos cada premissa em uma linha, com a letra P ao lado, para indicar que elas são premissas. Cada linha deve
estar enumerada. 

Vimos pela regra da Dupla Negação que “~~p” é a mesma coisa que “p”. Assim, podemos aplicar esta regra sobre a linha 3 para 
obter “~~p” a partir de “p”. Desta maneira, fica fácil aplicar a regra Modus Tolens sobre 1 e 4 e obter a conclusão “~p”. 

Perceba que para cada derivação feita, marcamos ao lado qual foi a regra aplicada e sobre qual/quais linhas ela foi aplicada.

2. Verificar que o argumento p → q, p ^ r ├ q é válido.
```diff
1) p → q     P
2) p ^ r     P
______________
3) p         2 - S
4) q         1, 3 - MP
```
Aplicando a regra da Simplificação sobre a linha 2, obtemos “p”. Em seguida aplicamos a regra Modus Ponens sobre as linhas
1 e 3 e obtemos “q”. 

3. Verificar que o argumento p ^ q, p v r → s ├ p ^ s é válido.
```diff
1) p ^ q         P
2) p v r → s     P
__________________
3) p             1 - S
4) p v r         3 - A
5) s             2, 4 - MP
6) p ^ s         3, 5 - U
```
Pela regra da Simplificação na linha 1, é possível obter “p”. Pela regra da Adição podemos adicionar a proposição “r” 
obtendo “p v r”. Aplicando Modus Ponens sobre 2 e 4 é possível extrair “s”. Com a regra da União, juntamos “p” e “s” e 
temos a conclusão “p ^ s”.

4. Verificar que o argumento p → (q → r), p → q, p ├ r é válido.
```diff
1) p → (q → r)   P
2) p → q         P
3) p             P
__________________
4) q → r         1, 3 - MP
5) q             2, 3 - MP
6) r             4, 5 - MP
```
Aplicando a regra Modus Ponens em 1 e 3 temos “q → r”. Aplicando Modus Ponens em 2 e 3, temos “q”. Aplicando Modus Ponens 
em 4 e 5 temos “r”.

5. Provar ~s a partir das premissas:

1) t

2) t → ~q

3) ~q → ~s    

```diff
1) t         P    
2) t → ~q    P
3) ~q → ~s   P
______________
4) ~q        1, 2 - MP
5) ~s        3, 4 - MP
``` 

6. Provar r v ~s a partir das premissas:

1) s ^ q

2) t → ~q

3) ~t → r

```diff
1) s ^ q     P
2) t → ~q    P
3) ~t → r    P
______________
4) q         1 - S
5) ~~q       2 - DN
6) ~t        2, 5 - MT
7) r         3, 6 - MP
8) r v ~ s   7 - A
```

7. Provar q a partir das premissas:

1) ~p v q

2) p

Pela Lei da condicional sabemos que “~p v q” é equivalente a “p → q”. Podemos então reescrever: 

```diff
1) p → q    P
2) p        P
_____________
3) q        1, 2 - MP    
```

## Referências
- Daghlian, Jacob. **Lógica e Álgebra de Boole**. Editora Atlas. 4ª edição. 2009.



