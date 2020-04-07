## Formalizando argumentos

Para faciltar, primeiramente podemos escrever o argumento na forma padrão, colocando a conclusão na última linha. Por exemplo:
- Se Deus existe, então a vida tem significado. Deus existe. A vida tem significado.

Podemos reescrever:
```diff
Se Deus existe, então a vida tem significado.
Deus existe.
∴ A vida tem significado.
```
Em seguida, vamos estabelecer os símbolos proposicionais para cada proposição, por exemplo:
- p = Deus existe
- q = A vida tem significado

E então, traduzimos cada linha do argumento acima em fórmulas:
```diff
p -> q
p
∴ q
```
Para facilitar, este argumento pode ser também escrito na forma horizontal (que é muito comum de ser encontrada nos livros). Neste caso, 
vamos usar o símbolo ⊦ (traço de asserção) em vez de ∴ . Todas as fórmulas que correspondem à premissas vão ser escritas do lado esquerdo
do traço de asserção, separadas por vírgulas. A conclusão será escrita do lado direito do traço de asserção. Assim, o argumento acima fica:
```diff
p -> q, p ⊦ q
```

## Exemplos
1. Se o carro passasse em alta velocidade, seria detectado por esse radar. Mas, o carro não foi dectado pelo radar. Portanto, o carro não passou em alta velocidade.

Neste caso, temos uma proposição composta (com condicional): "Se o carro passasse em alta velocidade, seria detectado por esse radar". No caso de proposições compostas, quebramos elas em proposições simples e atribuímos uma letra para cada proposição simples:
```diff
Se o carro passasse em alta velocidade, seria dectado por esse radar.
O carro não foi detectado pelo radar.
∴ O carro não passou em alta velocidade.

p = O carro passou em alta velocidade.
q = O carro foi detectado por esse radar.

p -> q, ~q ⊦ ~p
```

2. A Terra está a aproximadamente 93 milhões de milhas do Sol. A Lua está a cerca de 250 mil milhas da Terra. Portanto, a Lua está a cerca de 250 mil milhas mais próxima do Sol do que está a Terra.
```diff
A Terra está a aproximadamente 93 milhões de milhas do Sol.
A Lua está a cerca de 250 mil milhas da Terra. 
∴ A Lua está a cerca de 250 mil milhas mais próxima do Sol do que está a Terra.

p = A Terra está a aproximadamente 93 milhões de milhas do Sol.
q = A Lua está a cerca de 250 mil milhas da Terra. 
r = A Lua está a cerca de 250 mil milhas mais próxima do Sol do que está a Terra.

p, q ⊦ r
```

3. Eu segui a receita que estava na caixa, mas a sobremesa ficou com um gosto horrível. Portanto, algum ingrediente devia estar
estragado ou eu errei alguma etapa.
```diff
Eu segui a receita que estava na caixa. 
A sobremesa ficou com um gosto horrível. 
∴ Algum ingrediente devia estar estragado ou eu errei alguma etapa.

p = Eu segui a receita que estava na caixa. 
q = A sobremesa ficou com um gosto horrível. 
r = Algum ingrediente devia estar estragado.
s = Eu errei alguma etapa.

p ^ q ⊦ r v s
```

4. Não foi o mordomo e nem a criada. Pode ter sido o motorista ou o cozinheiro. O motorista estava no aeroporto quando o assassino
agiu. O cozinheiro é o único que não tem álibi. Além disso, a herdeira foi envenenada. É lógico concluir que o cozinheiro foi o
culpado.
```diff
Não foi o mordomo e nem a criada. 
Pode ter sido o motorista ou o cozinheiro. 
O motorista estava no aeroporto quando o assassino agiu. 
O cozinheiro é o único que não tem álibi. 
A herdeira foi envenenada. 
∴ O cozinheiro foi o culpado.

p = Foi o mordomo.
q = Foi a criada.
r = Foi o motorista.
s = Foi o cozinheiro / O cozinheiro foi o culpado.
t = O motorista estava no aeroporto quando o assassino agiu.
u = O cozinheiro é o único que não tem álibi.
v = A herdeira foi envenenada.

~p ^ ~q, r v s, t, u, v ⊦ s
```

## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.
