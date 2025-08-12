# 🚗 Estacionamento Automático com Barreira

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/08977e67-7f50-4dbc-851b-4032ed77bb25" />

## 1. Definição do Problema (Cenário Real)

A cancela só abre se:
1. O **sensor de presença** detectar um carro (**C = 1**)
2. A **tag** for lida com sucesso (**T = 1**)
3. O **pagamento** estiver autorizado (**P = 1**)

---

## 2. Variáveis de Entrada

| Variável | Significado |
|----------|-------------|
| **C** | Carro presente (1 = sim, 0 = não) |
| **T** | Tag lida com sucesso (1 = sim, 0 = não) |
| **P** | Pagamento autorizado (1 = sim, 0 = não) |
| **S** | Cancela abre (1 = sim, 0 = não) |

---

## 3. Tabela Verdade

| C (Carro) | T (Tag) | P (Pagamento) | S (Cancela abre) |
|:---------:|:-------:|:--------------:|:----------------:|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

---

## 4. Expressão Canônica (Soma de Mintermos)

A saída **S** só é 1 quando **C = 1**, **T = 1** e **P = 1**:

`S = C · T · P`


---
## 5. Mapa de Karnaugh
## 6. Expressão Simplificada
## 7. Circuito Lógico

---

## 8. Lógica do Circuito (Explicação)

A cancela **só será aberta** quando:
- Um carro estiver presente (**C = 1**)
- A tag for lida corretamente (**T = 1**)
- O pagamento for aprovado (**P = 1**)

---

## 9. Simulação



## Circuito Lógico

Componentes:
- 3 entradas (Switches)
- 2 portas AND (ou 1 AND de 3 entradas)
- 1 saída (LED)

---

## Exemplo:

`C (Carro)`	<br>
`T (Tag)`	<br>
`P (Pagamento)`	<br>
`S (Cancela abre)` <br>

```text
C ───┐
     AND ───┐
T ───┘     AND ─── S
            |
P ──────────┘
```
