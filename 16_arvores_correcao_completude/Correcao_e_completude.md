## Árvores de refutação: correção e completude
Uma vez que estudamos como montar as árvores, podemos analisar a relação das propriedades da lógica proposicional com árvores 
de refutação / tableaux semânticos.

### Teorema da correção
Dada uma fórmula H da lógica proposicional, se existe uma árvore de refutação / tableau semântico fechada
(contém todos os ramos fechados) associado a ~H, então H é uma tautologia.

### Teorema da completude
Dada uma fórmula H da lógica proposicional, se não existe uma árvore de refutação / tableau semântico 
fechada associado a ~H, então H não é uma tautologia. 

### Exemplos
a) Verificar se a fórmula (p -> q) v (p ^ ~q) é tautologia:

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/16_arvores_correcao_completude/exemplo_1.png)

Os dois ramos são fechados, então a fórmula é tautologia.

b) Verificar se a fórmula ~(q -> (p ^ ~p)) é tautologia:

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/16_arvores_correcao_completude/exemplo_2.png)

Um ramo ficou aberto e um ramo ficou fechado, então a fórmula não é tautologia.

### Observações
1) O fato de uma árvore montada com ~H ter todos os ramos abertos, não quer dizer que H é uma contradição. Assim como o fato de a árvore ter ramos abertos e fechados não quer dizer que H é uma contingência. 

Considere, por exemplo, a fórmula: p ^ (p -> q)

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/16_arvores_correcao_completude/exemplo_3.png)

Nenhum ramo fecha. Se a tabela-verdade da fórmula for construída:

| **p** | **q** | **(p -> q)** | **p ^ (p -> q)** |
|-------|-------|--------------|------------------|
| V     | V     | V            | V                |
| V     | F     | F            | F                |
| F     | V     | V            | F                |
| F     | F     | F            | F                |

A fórmula resulta em contingência. O exemplo mostra que:

- Uma contingência nem sempre terá uma árvore com ramos abertos e fechados.
- Uma árvore com todos os ramos abertos nem sempre vem de uma fórmula que é uma contradição.
- **Será possível afirmar apenas que a fórmula não é tautologia, nada além disso.**

2) O que acontece se a árvore é construída a partir de H em vez de ~H? 
- H é equivalente à ~(~H). 
- Sendo assim, ao montar a árvore com H, pode-se dizer que tem-se a árvore de ~(~H).
- Se a árvore de ~(~H) tiver todos os ramos fechados, quer dizer que ~H é tautologia.  
- Se ~H é tautologia, então H é uma contradição. 
- **Ou seja, dada uma fórmula H, se existe uma árvore fechada associada a H, então H é uma contradição.** 

## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.
- Souza, J. N. de. **Lógica para ciência da computação e áreas afins**, Elsevier, Rio de Janeiro, 2015.
- Site para gerar árvores: http://www.formallogic.com/en/truth-tree-solver/
