## Regras de inferência

### União - U
```diff
p
q
_____
p ^ q
```

### Simplificação - S
```diff
p ^ q
_____
p
q
```

### Modus Ponens - MP
```diff
p → q
p
_
q
```

### Adição - A
```diff
p 
_____
p v q
```

### Silogismo Hipotético - SH
```diff
p → q
q → r
_____
p → r 
```

### Modus Tolens - MT
```diff
p → q
~q
__
~p
```

### Silogismo Disjuntivo - SD
```diff
p v q
~p
__
q
```

### Eliminação da Bicondicional - Ebic
```diff
p ↔ q
_________________
(p → q) ^ (q → p)
```

### Introdução da Bicondicional - Ibic
```diff
(p → q) ^ (q → p)
_________________
p ↔ q
```

### Dilema Construtivo - DC
```diff
p → q
r → s
p v r
_____
q v s
```

### Dilema Construtivo (caso particular)
```diff
p → q
r → q
p v r
_____
q
```

### Dilema Destrutivo - DD
```diff
p → q
r → s
~q v ~s
_______
~p v ~r
```

### Dupla Negação - DN
```diff
~~p
___
p
```

### Regra da Absorção - RA ou ABS
```diff
p → q
___________
p → (p ^ q)
```

### Simplificação Disjuntiva - Sv
```diff
p v r
p v ~r
______
p
```












