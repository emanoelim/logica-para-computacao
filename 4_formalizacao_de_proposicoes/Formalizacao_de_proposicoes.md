## Formalizando proposições

Processo pelo qual convertemos proposições ou argumentos em fórmulas. A formalização de sentenças simples é fácil, basta atribuir à sentença um símbolo proposicional. Por exemplo:
- Hoe está chovendo = p

Para proposições compostas, devemos quebrá-las nas proposições simples que as foram, atribuindo um símbolo proposicional para cada uma dessas proposições simples. Por exemplo:

**a.** Proposição com conjunção: definimos uma letra para o 1º conjunto e outra para o 2º conjuncto. Por ex.: "hoje está chovendo e nevando".

1º conjuncto = hoje está chovendo = p

2º conjuncto = hoje está nevando = q

logo, temos:

p ^ q

**b.** Proposição com disjunção: definimos uma letra para o 1º disjuncto e outra para o 2º disjuncto. Por ex.: "hoje está chovendo ou nevando".

1º disjuncto = hoje está chovendo = p

2º disjuncto = hoje está nevando = q

logo, temos:

p v q


**c.** Proposição com implicação: definimos uma letra para o antecedente e outra para o consequente. Por ex.: "hoje está chovendo e nevando".

Antecedente = hoje está chovendo = p

Consequente = hoje está nevando = q

logo, temos:

p -> q

**d.** Proposição com bi implicação: definimos uma letra para o antecedente e outra para o consequente. Por ex.: "hoje está chovendo e nevando".

Antecedente = hoje está chovendo = p

Consequente = hoje está nevando = q

logo, temos:

p <-> q

**e.** Proposição com negação: sempre que a sentença estiver negada, colocamos o simbolo de negação antes da letra. Exemplos:
- Hoje não está chovendo.
- É mentira que hoje está chovendo.
- É falso que hoje está chovendo.
- Não é verdade que hoje está chovendo...

Se "hoje está chovendo" = p, então todas as formas negadas acima podem ser representadas por ~p.

Quando as sentenças tem vários operadores lógicos é preciso tomar mais cuidado. Por exemplo: "Hoje não é, ambos, segunda-feira e terça-feira.". Considerando que:
- p = hoje é segunda-feira
- q = hoje é terça-feira

Não podemos simplesmente escrever: ~p ^ q, pois isso levaria um leitor a entender que: "Hoje não é segunda-feira e é terça-feira.". Para que o leitor entenda que hoje não é nenhum dos dois dias da semana, a negação deve se aplicar às duas proposições. Para isso podemos usar os parêntestes: ~(p ^ q). Funciona como na matemática: quando lemos a fórmula -(2x + y), sabemos que o sinal negativo aplica-se aos dois termos.

Também precisamos de mais cuidado quando a proposição é composta por mais de duas proposições simples. A sentença: "Hoje é segunda-feira, ou hoje é terça-feira e dia de eleição" necessita dos parênteses ao ser formalizada para que seu sentido fique claro para o leitor. Se considerarmos que:
- p = hoje é segunda-feira
- q = hoje é terça-feira
- r = hoje é dia de eleição

Devemos escrever: p v (q ^ r). Se os parênteses fossem omitidos, escrevendo p v q ^ r, o leitor poderia interpretar: "Hoje é segunda-feira ou terça-feira, e hoje é dia de eleição.". Na forma com os parênteses fica claro que a eleição acontece na terça-feira, enquanto na forma sem os parênteses isso não fica claro.

### Exemplo resolvido
1. Interprete a letra "c" como "está chovendo" e a letra "n" como "está nevando". Converta em fórmulas:

a. Está chovendo.

c
___
b. Não está chovendo.

~c
___
c. Está chovendo ou nevando.

c v n
___
d. Está chovendo e nevando.

c ^ n
___
e. Está chovendo mas não está nevando.

c ^ ~n
___
f. Não é o caso que está chovendo e nevando.

~(c ^ n)
___
g. Se não está chovendo, então está nevando.

~c -> n
___
h. Não é o caso que se está chovendo, então está nevando.

~(c -> n)
___
i. Não é o caso que se está nevando, então está chovendo.

~(n -> c)
___
j. Está chovendo se e esomente se não está nevando.

c <-> ~n
___
k. Não é o caso que está chovendo ou nevando.

~(c v n)
___
l. Se está nevando e chovendo, então está nevando.

(c ^ n) -> n
___
m. Se não está chovendo, então não é o caso que está nevando e chovendo.

~c -> ~(n ^ c)
___
n. Está chovendo, ou está nevando e chovendo.

c v (n ^ c)
___
o. Está chovendo e nevando, ou está nevando mas não está chovendo.

(c ^ n) v (n ^ ~c)

## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.



