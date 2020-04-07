## Lógica proposicional
Estuda técnicas de lógica que permitem verificar a veracidade dos argumentos.

Baseia-se em 3 passos principais:
- Especificar uma linguagem para representar o conhecimento.
- Estudar métodos que produzem ou verificam a validade dos argumentos.
- Definir sistemas de dedução que permitem derivar o conhecimento para chegar a uma conclusão.

### Linguagem
O primeiro passo no estudo da lógica proposicional é definir o conjunto de símbolos que ele utilizará, ou o seu **alfabeto**. Este
alfabeto é composto de:
- Sinais de pontuação: ()
- Símbolos proposicionais - para representar as proposições: p, q, r, s …
- Conectivos proposicionais: 
  - disjunção (ou): v
  - conjunção (e): ^
  - condicional (pode ser lido como “implica em”): →
  - bicondicional (pode ser lido como “bi-implica em”): ↔
  - negação (pode ser lido como “não” ou “negação de”): ~
  
### Fórmulas
As fórmulas da lógica proposicional seguem algumas regras:
1. Todo símbolo proposicional é uma fórmula:
  - **p** é uma fórmula
  - **q** é uma fórmula
  - **r** é uma fórmula
  
 2. Se **p** é uma fórmula, então sua negação também é:
  - ~p
 
 3. Se **p** e **q** são fórmulas, então a disjunção, conjunção, implicação e bi-implicação entre **p** e **q** também são fórmulas:
  - (p v q)
  - (p ^ q)
  - (p → q)
  - (p ↔ q)
  
 ### Fórmulas bem formadas (wffs)
 Uma fórmula é bem formada, ou uma wff (*well-formed formula*) quando ela segue as regras acima. Qualquer fórmula que não segue essas
 regras não é considerada uma wff. As wffs complexas são formadas a partir das simples, por aplicações repetidas das regras de formação.
 
 Por exemplo, pela regra 1, vemos que p e q são wffs. Segue pela regra 3 que p ^ q é uma wff. Daí, pela regra 2, tem-se que ~(p ^ q) 
 também é uma wff. E assim por diante.
 
 **Exceção**: pela regra, quando unimos dois simbolos proposicionais com um conectivo, também adicionamos um par de parênteses. Sendo assim, 
 (p ^ q) seria uma wff, enquanto p ^ q não seria. Entretanto, nesta situação, os parênteses não são fundamentais para tornar claro o 
 significado da fórmula. Fazendo uma analogia com a matemática, a fórmula (2 + 2) levaria ao resultado 4, assim como a fórmula 2 + 2.
 Portanto, vamos adotar a convenção de que os parênteres externos podem ser omitidos.
 
## Referências
- Nolt, J., Rohatyn, D. **Lógica**, McGraw-Hill, São Paulo, 1991.
