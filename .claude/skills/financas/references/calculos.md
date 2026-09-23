# Cálculos úteis

Mostre a conta para a pessoa. Use Python/Bash quando precisar de precisão.

## Juros compostos
Saldo futuro = P × (1 + i)^n   (i ao mês em decimal, n em meses)

Taxa mensal → anual: (1 + i_m)^12 − 1.  Ex.: 14% a.m. → ~381% a.a.
Taxa anual → mensal: (1 + i_a)^(1/12) − 1.

## Parcela de um financiamento (Price)
PMT = P × i / (1 − (1 + i)^−n)

## Quanto tempo para quitar pagando X por mês
n = −ln(1 − P·i / X) / ln(1 + i)   (se X ≤ P·i, a dívida nunca acaba — sinalize!)

## À vista vs. parcelado (negociação)
Descubra a taxa implícita do parcelamento (resolver i em PMT) e compare com o que o dinheiro
renderia guardado. Regra prática: se a pessoa **tem** o dinheiro à vista sem tocar a reserva
mínima, e o desconto à vista é grande, pague à vista. Se não tem, a parcela que cabe com folga
é melhor que um acordo à vista que zera o caixa.

## Vale a pena trocar dívida A por B?
Compare o **custo total restante**: soma das parcelas restantes de A vs. soma das parcelas de B
(+ tarifas, IOF, seguro embutido = CET). Troque só se B for menor e o prazo não esticar demais.

## Exemplo em Python
```python
import math
def parcela(P, i, n): return P * i / (1 - (1 + i) ** -n)
def meses_para_quitar(P, i, X):
    if X <= P * i: return math.inf
    return -math.log(1 - P * i / X) / math.log(1 + i)
print(round(parcela(5000, 0.03, 12), 2))          # 502.31
print(math.ceil(meses_para_quitar(5000, 0.14, 800)))  # rotativo 14% a.m.
```
