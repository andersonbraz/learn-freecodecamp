# ES6: explore as diferenças entre as palavras-chave var e let

Um dos maiores problemas ao declarar variáveis ​​com a palavra-chave **var** é que você pode sobrescrever declarações de variáveis ​​sem erro.

```javascript
var camper = 'James';
var camper = 'David';
console.log(camper);
// logs 'David'
```

Como você pode ver no código acima, a variável **camper** é originalmente declarada com valor igual a James, em seguida, substituída por David. Em um aplicativo pequeno, você pode não encontrar esse tipo de problema, mas quando seu código se torna maior, você pode substituir acidentalmente uma variável que não pretendia sobrescrever. Como esse comportamento não gera um erro, pesquisar e corrigir erros se torna mais difícil.
Uma nova palavra-chave chamada **let** foi introduzida no ES6 para resolver esse possível problema com a palavra-chave **var**. Se você fosse substituir **var** com **let** nas declarações de variáveis do código acima, o resultado seria um erro.

```javascript
let camper = 'James';
let camper = 'David'; // throws an error
```

Este erro pode ser visto no console do seu navegador. Portanto **var**, diferentemente, ao usar **let**, uma variável com o mesmo nome pode ser declarada apenas uma vez. Observe o "use strict". Isso habilita o Modo Estrito, que detecta erros comuns de codificação e ações "inseguras". Por exemplo:

```javascript
"use strict";
x = 3.14; // throws an error because x is not declared
```
---

## Desafio:

Atualize o código para que ele use apenas a palavra-chave **let**.