# Questão 2 - Seleção múltipla

## Código original

```c
if ((k == 1) || (k == 2)) j = 2 * k - 1;
if ((k == 3) || (k == 5)) j = 3 * k + 1;
if (k == 4) j = 4 * k - 1;
if ((k == 6) || (k == 7) || (k == 8)) j = k - 2;
```

A lógica do código original pode ser reescrita usando uma estrutura de seleção múltipla, evitando vários testes `if` separados.

---

## a. C

```c
switch (k) {
    case 1:
    case 2:
        j = 2 * k - 1;
        break;

    case 3:
    case 5:
        j = 3 * k + 1;
        break;

    case 4:
        j = 4 * k - 1;
        break;

    case 6:
    case 7:
    case 8:
        j = k - 2;
        break;
}
```

---

## b. Ruby

```ruby
case k
when 1, 2
  j = 2 * k - 1
when 3, 5
  j = 3 * k + 1
when 4
  j = 4 * k - 1
when 6, 7, 8
  j = k - 2
end
```

---

## c. Erlang

```erlang
J =
  case K of
    1 -> 2 * K - 1;
    2 -> 2 * K - 1;
    3 -> 3 * K + 1;
    5 -> 3 * K + 1;
    4 -> 4 * K - 1;
    6 -> K - 2;
    7 -> K - 2;
    8 -> K - 2
  end.
```

---

## Discussão

Nessa questão, achei Ruby a linguagem mais simples de entender. O case when ficou bem limpo, principalmente porque dá para colocar vários valores na mesma linha, como when 1, 2, sem precisar usar break.

Em C, o switch também é fácil de entender, mas achei um pouco mais trabalhoso porque precisa ficar colocando break em cada caso. Se esquecer o break, o código pode dar um resultado errado.

Já em Erlang, a estrutura funciona, mas achei menos familiar. Como a linguagem trabalha de uma forma mais funcional, em vez de simplesmente mudar o valor de j, ela retorna um valor para J. Para quem está mais acostumado com C, Java ou Python, isso parece um pouco diferente.

Na minha opinião, Ruby ficou melhor nessa questão, porque foi a linguagem mais clara e menos carregada de símbolos.
