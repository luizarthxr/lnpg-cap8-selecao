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

Na minha opinião, o Python foi a linguagem mais fácil de escrever nessa questão, porque o código fica menor e mais direto. Não precisa colocar muita coisa, como chaves ou declaração de tipo, então fica mais simples de montar.

Achei Java e Swift também fáceis de entender, porque usam o while de uma forma bem parecida com o pseudocódigo. A diferença é que eles têm uma estrutura mais formal, com chaves, o que deixa o bloco bem separado.

Já Haskell foi o mais difícil para mim, porque ele não segue tanto essa ideia de ir alterando o valor das variáveis como nas outras linguagens. Precisa usar recursão, então ficou menos intuitivo.

Para mim, a melhor combinação entre facilidade de escrita e leitura foi o Python.
