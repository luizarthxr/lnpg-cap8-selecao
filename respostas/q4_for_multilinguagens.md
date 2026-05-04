# Questão 4 - Construção `for` em 5 linguagens

## Código original em Java

```java
int i, j, n = 100;

for (i = 0, j = 17; i < n; i++, j--)
  sum += i * j + 3;
```

A lógica do código original consiste em iniciar `i` com 0, `j` com 17 e repetir o laço enquanto `i < n`. A cada repetição, `i` aumenta uma unidade e `j` diminui uma unidade.

Foram escolhidas as seguintes linguagens:

- C;
- Python;
- JavaScript;
- Ruby;
- Swift.

---

## 1. C

```c
int i, j, n = 100;
int sum = 0;

for (i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
}
```

---

## 2. Python

```python
n = 100
j = 17
sum = 0

for i in range(n):
    sum += i * j + 3
    j -= 1
```

---

## 3. JavaScript

```javascript
let n = 100;
let sum = 0;

for (let i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
}
```

---

## 4. Ruby

```ruby
n = 100
j = 17
sum = 0

for i in 0...n
  sum += i * j + 3
  j -= 1
end
```

---

## 5. Swift

```swift
let n = 100
var j = 17
var sum = 0

for i in 0..<n {
    sum += i * j + 3
    j -= 1
}
```

---

## Discussão
C e JS foram as linguagens mais parecidas com Java, porque permitem colocar a inicialização, a condição e o incremento/decremento direto dentro do for. Isso deixou o código bem próximo do exemplo original.

Python ficou mais simples visualmente, mas precisou colocar o j -= 1 dentro do laço, porque o for dele funciona usando range. Mesmo assim, achei bem fácil de entender.

Ruby também ficou parecido com Python, usando intervalo. O código é curto e legível, mas também precisa diminuir o valor de j dentro do bloco.

Swift usa uma estrutura de intervalo bem clara, com 0..<n. Achei organizado, mas também um pouco diferente do for tradicional de Java.

Para mim, JavaScript foi a melhor opção quando penso em proximidade com Java. Mas, olhando só para simplicidade, Python foi o mais fácil de ler.

A melhor combinação entre proximidade com Java e clareza é JavaScript, enquanto a melhor simplicidade visual é Python.
