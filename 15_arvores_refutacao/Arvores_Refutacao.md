## Árvores de refutação ou tableuax semânticos

Uma árvore de refutação, ou tableau semântico, é um método que permite verificar se um argumento é válido ou não (entre outros). 
Para testar a validade de um argumento usando uma árvore de refutação, deve-se montar uma lista com as premissas e a negação da conclusão. 
Essa lista irá constituir a raíz da árvore. Em seguida aplicamos regras sobre essas premissas até que cada premissa seja desmembrada em 
símbolos proposicionais ou suas negações, ou até que encontremos contradições em todos os ramos da árvore.

Se algum ramo da árvore não tem uma contradição, refutamos o argumento, ou seja, dizemos que ele é inválido. Se todos os ramos da árvore
têm uma contradição, então a tentativa de refutar o argumento falhou. Logo, podemos concluir que o argumento é válido.

Este método lembra a prova por contradição / redução ao absurdo. Na prova por contradição, adicionamos a negação da conclusão como
hipótese e buscamos por uma contradição. Dependendo das regras de inferência que forem aplicadas, existem caminhos diferentes para
encontrar a contradição. Quando construimos uma árvore de refutação, ao criar as ramificações da árvore, o que estemos fazendo é testar todos os caminhos possíveis. Se em todos esses caminhos for possível encontrar uma contradição, então o argumento não tem como ser inválido.

### Regras para árvores de refutação ou tableuax semânticos

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/regras_arvores.PNG)

### Definições
- **Ramo fechado:** o ramo é fechado se ele contém uma fórmula e a sua negação, ou seja, uma contradição.
- **Ramo saturado:** não é mais possível aplicar nenhuma regra no ramo.
- **Ramo aberto:** um ramo é aberto quando ele é saturado e não é fechado.

## Exemplos

a) Verificar se o argumento é válido: p ^ q ⊢ ~~p

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_a.PNG)

- A negação da conclusão ~~p entra como premissa na raíz da árvore.
- Assim como na prova direta convém enumerar as linhas e indicar qual regra foi aplicada.
- A medida que desmembramos uma fórmula, podemos riscá-la ou fazer uma marca indicando que a mesma já foi usada. Cada fórmula recebe a aplicação de somente uma regra.
- Quando encontramos um ramo fechado, marcamos o ramo com um X.
- Como o único ramo da árvore é fechado (contém a contradição p e ~p), a tentativa de refutar o argumento falhou. Nesse caso dizemos 
que o argumento é válido.

b) Verificar se o argumento é válido: p v q, ~p ⊢ q

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_b.PNG)

- A negação da conclusão q entra como premissa na raíz da árvore.
- Como as premissas ~p e ~q já são símbolos proposicionais negados, não é necessário aplicar regra sobre elas. Precisamos apenas desmembrar a premissa p v q.
- Como os dois ramos da árvore são fechados (o primeiro ramo contém a contradição ~p e p, o segundo ramo tem a contradição ~q e q), a tentativa de refutar o argumento falhou. Nesse caso dizemos que o argumento é válido.

c) Verificar se o argumento é válido: p v q, p ⊢ ~q

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_c.PNG)

- A negação da conclusão ~q entra como premissa na raíz da árvore.
- Como as premissas p e q já são símbolos proposicionais, não é necessário aplicar regra sobre elas. Precisamos apenas desmembrar a premissa p v q.
- Como os dois ramos da árvore são abertos, a tentativa de refutar o argumento teve suceso. Nesse caso dizemos que o argumento é inválido.

d) Verificar se o argumento é válido: p -> q, q -> r, p ⊢ r

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_d.PNG)

- A negação da conclusão r entra como premissa na raíz da árvore.
- Como as premissas p e ~r já são símbolos proposicionais ou negações de símbolos proposicionais, não é necessário aplicar regra sobre elas. Precisamos apenas desmembrar as premissas p -> q e q -> r.
- Ao desmembrar a premissa p -> q, já encontramos um ramo fechado (devido a contradição p e ~p). Ainda precisamos desmembrar q -> r. Isso é feito no ramo que ainda está aberto.
- Após desmembrar q -> r, os outros dois ramos se fecham, o do meio com q e ~q e o último com r e ~r.
- Como os três ramos da árvore são fechados, a tentativa de refutar o argumento falhou. Nesse caso dizemos que o argumento é válido.

e) Verificar se o argumento é válido: p <-> q, ~p ⊢ ~q

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_e.PNG)

- A negação da conclusão ~q entra como premissa na raíz da árvore.
- Como a premissa ~p já é um símbolo proposicional, não é necessário aplicar regra sobre ela. Precisamos apenas desmembrar as premissas p <-> q e ~~q.
- Ao desmembrar a premissa p <-> q, já encontramos dois ramos fechados (o primeiro com p e ~p e o segundo com q e ~q). 
- Como os dois ramos da árvore são fechados, a tentativa de refutar o argumento falhou. Nesse caso dizemos que o argumento é válido.

f) Verificar se o argumento é válido: ~(p ^ q) ⊢ ~p ^ ~q

![all text](https://github.com/emanoelim/LC21CP_2020_1/blob/master/15_arvores_refutacao/exe_f.PNG)

- A negação da conclusão ~p ^ ~q entra como premissa na raíz da árvore.
- Após desmembrar a premissa ~(p ^ q) conseguimos obter dois símbolos proposicionais negados, mas ainda existe uma premissa que precisa ser desmembrada. Como os dois ramos existentes estão abertos, desmembramos a premissa nos dois ramos.
- Como a árvore ficou com dois ramos fechados e dois abertos, a tentativa de refutar o argumento teve sucesso, logo o argumento é inválido.

## Observações
- As regras aplicam-se somente a fórmulas inteiras. O exemplo abaixo deve ser evitado:
```diff
p ^ ~~q
p ^ q		   1, R5
```
- Embora remover esta dupla negação não leve a um resultado incorreto, não é necessário fazer isso. Problemas mais sérios podem ocorrer aplicando outras regras, como a R1 ou R2.

- A ordem na qual as regras são aplicadas é indiferente, mas ficará mais fácil se aplicarmos primeiramente regras que não geram bifurcação (a árvore ficará com menos ramos).

## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.






