# Questão 1 - Reescrita usando laço

## Pseudocódigo original

```text
k = (j + 13) / 27
loop:
if k > 10 then goto out
  k = k + 1
  i = 3 * k - 1
  goto loop
out: ...
```

A lógica do código original pode ser representada por um laço que continua executando enquanto `k <= 10`. Quando `k` passa a ser maior que 10, o laço termina.

---

## a. Java

```java
int k = (j + 13) / 27;

while (k <= 10) {
    k = k + 1;
    i = 3 * k - 1;
}
```

---

## b. Python

```python
k = (j + 13) // 27

while k <= 10:
    k = k + 1
    i = 3 * k - 1
```

---

## c. Haskell

```haskell
loop :: Int -> Int -> (Int, Int)
loop k i
  | k > 10 = (k, i)
  | otherwise =
      let novoK = k + 1
          novoI = 3 * novoK - 1
      in loop novoK novoI

programa :: Int -> Int -> (Int, Int)
programa j iInicial =
  let k = (j + 13) `div` 27
  in loop k iInicial
```

---

## d. Swift

```swift
var k = (j + 13) / 27

while k <= 10 {
    k = k + 1
    i = 3 * k - 1
}
```

---

## Discussão

Para esse código, a linguagem com melhor facilidade de escrita é Python, pois sua sintaxe é mais curta e direta. O uso do `while` deixa a lógica simples de entender, e não há necessidade de declarar tipos ou usar chaves para delimitar blocos.

Em relação à legibilidade, Java, Python e Swift são bastante claros, porque todos utilizam uma estrutura `while` parecida com o pseudocódigo original. Java e Swift deixam o bloco mais explícito por causa das chaves, enquanto Python usa indentação, o que torna o código mais limpo visualmente.

Haskell é a linguagem menos direta para esse exemplo, pois o código original segue um estilo imperativo, com alteração de valores ao longo da execução. Como Haskell trabalha melhor com programação funcional, a solução foi feita usando recursão.

Assim, para esse caso específico:

- melhor facilidade de escrita: Python;
- melhor legibilidade: Python ou Swift;
- melhor combinação entre facilidade de escrita e legibilidade: Python.
