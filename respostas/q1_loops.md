# Questão 1 - Reescrita usando laço

Pseudocódigo original:

```text
k = (j + 13) / 27
loop:
if k > 10 then goto out
  k = k + 1
  i = 3 * k - 1
  goto loop
out: ...

Java: 

int k = (j + 13) / 27;

while (k <= 10) {
    k = k + 1;
    i = 3 * k - 1;
}
