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

Em C, o uso de `switch` é bastante tradicional e direto. Ele permite organizar os casos de forma clara, agrupando valores que executam a mesma instrução. Porém, é necessário usar `break` ao final de cada grupo de casos para evitar que a execução continue nos próximos blocos.

Em Ruby, a estrutura `case when` fica mais simples e legível. A linguagem permite agrupar vários valores em uma mesma linha, como `when 1, 2`, sem a necessidade de usar `break`. Isso deixa o código mais limpo e fácil de ler.

Em Erlang, a estrutura `case` também resolve o problema, mas de uma forma mais funcional. Como as variáveis em Erlang são imutáveis, o valor de `J` é definido a partir do resultado da expressão `case`. Para quem está acostumado com linguagens imperativas, essa forma pode parecer menos direta.

Para esse código específico:

- C é direto, mas mais verboso por causa dos `break`;
- Ruby é mais conciso e legível;
- Erlang é correto, mas exige adaptação ao estilo funcional.

A linguagem que apresenta a melhor combinação entre clareza e concisão, nesse caso, é Ruby.
