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

O principal desafio que eu vi foi tirar o break sem mudar a lógica do programa. Para resolver isso, usei uma variável de controle chamada continuar, que serve para dizer se o laço deve continuar rodando ou parar.

Achei Python o mais simples de escrever, porque o código fica mais limpo e fácil de acompanhar. A indentação ajuda a enxergar onde começa e termina cada parte.

JavaScript ficou parecido com C, então também é fácil de comparar com o código original. Porém, ele tem mais símbolos, como chaves, ponto e vírgula e operadores com três iguais.

Kotlin foi o que eu achei mais organizado na parte da seleção, porque o when deixa os casos bem separados e fáceis de ler.

No geral, eu diria que Python foi o mais fácil de escrever, mas Kotlin ficou com a melhor organização visual.
