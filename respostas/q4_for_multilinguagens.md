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

Em C, a construção do `for` é muito parecida com Java. A linguagem permite inicializar `i` e `j`, definir a condição do laço e atualizar as duas variáveis diretamente no cabeçalho do `for`. Por isso, a solução em C fica muito próxima do código original.

Em JavaScript, a estrutura também é bastante semelhante à de Java. É possível declarar `i` e `j` no próprio cabeçalho do `for`, além de usar `i++` e `j--`. Isso torna JavaScript uma das linguagens mais próximas do exemplo original.

Em Python, o laço é baseado em `range(n)`. Por isso, o controle de `i` é feito automaticamente, mas o decremento de `j` precisa ser colocado dentro do corpo do laço. A escrita é simples e legível, embora não seja tão parecida com o `for` de Java.

Em Ruby, a ideia é semelhante à de Python, usando um intervalo de valores. O intervalo `0...n` percorre os valores de 0 até 99, considerando que `n = 100`. Assim como em Python, o decremento de `j` é feito dentro do laço.

Em Swift, o laço também usa intervalo, com a construção `0..<n`. A sintaxe é clara e organizada, mas o decremento de `j` também precisa ficar dentro do corpo do laço.

Para esse código específico:

- C e JavaScript são as linguagens mais parecidas com Java;
- Python é a mais simples visualmente;
- Ruby também é concisa e fácil de entender;
- Swift tem boa legibilidade e uma sintaxe organizada.

A melhor combinação entre proximidade com Java e clareza é JavaScript, enquanto a melhor simplicidade visual é Python.
