# Questão 3 - Reescrita sem goto ou break

## Código original em C

```c
j = -3;

for (i = 0; i < 3; i++) {
  switch (j + 2) {
    case 3:
    case 2:
      j--;
      break;

    case 0:
      j += 2;
      break;

    default:
      j = 0;
  }

  if (j > 0)
    break;

  j = 3 - i;
}
```

O objetivo é reescrever o código sem usar `goto` ou `break`. Para isso, foi utilizada uma variável booleana de controle para indicar se o laço deve continuar ou parar.

Foram escolhidas as seguintes linguagens:

- Python;
- JavaScript;
- Kotlin.

---

## 1. Python

```python
j = -3
i = 0
continuar = True

while i < 3 and continuar:
    valor = j + 2

    if valor == 3 or valor == 2:
        j -= 1
    elif valor == 0:
        j += 2
    else:
        j = 0

    if j > 0:
        continuar = False
    else:
        j = 3 - i
        i += 1
```

---

## 2. JavaScript

```javascript
let j = -3;
let i = 0;
let continuar = true;

while (i < 3 && continuar) {
    let valor = j + 2;

    if (valor === 3 || valor === 2) {
        j--;
    } else if (valor === 0) {
        j += 2;
    } else {
        j = 0;
    }

    if (j > 0) {
        continuar = false;
    } else {
        j = 3 - i;
        i++;
    }
}
```

---

## 3. Kotlin

```kotlin
var j = -3
var i = 0
var continuar = true

while (i < 3 && continuar) {
    when (j + 2) {
        3, 2 -> j--
        0 -> j += 2
        else -> j = 0
    }

    if (j > 0) {
        continuar = false
    } else {
        j = 3 - i
        i++
    }
}
```

---

## Discussão

A principal mudança feita nessa questão foi substituir o `break` por uma variável de controle chamada `continuar`. Enquanto essa variável for verdadeira e `i` for menor que 3, o laço continua executando. Quando `j > 0`, a variável `continuar` recebe `False` ou `false`, encerrando o laço sem a necessidade de usar `break`.

Em Python, a solução ficou simples e direta, com pouca sintaxe e boa legibilidade. A indentação ajuda a visualizar os blocos de decisão e repetição.

Em JavaScript, a estrutura ficou parecida com linguagens como C e Java, utilizando chaves e ponto e vírgula. Mesmo sem usar `switch` e `break`, o código continua claro.

Em Kotlin, a estrutura `when` torna a seleção mais elegante e legível, pois permite substituir vários testes condicionais de forma organizada.

Para esse exemplo:

- Python tem a escrita mais simples;
- JavaScript é mais próximo da estrutura original em C;
- Kotlin apresenta a seleção mais legível por causa do `when`.

A melhor combinação entre legibilidade e organização, nesse caso, é Kotlin.
