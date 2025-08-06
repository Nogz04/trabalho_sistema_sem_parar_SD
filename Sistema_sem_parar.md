# O que vamos fazer?

> Entrada automática ao estacionamento com barreira (Tipo o sem parar)

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/08977e67-7f50-4dbc-851b-4032ed77bb25" />

# Como vai ser?

## Cenário:

> A cancela só abre se o sensor detectar um carro: (1 -> Detectado, 0 -> Não detectado) <br> E o pagamento tiver sido feito via QR code do carro. (1 -> Pagamento feito, 0 -> Pagamento não feito)

## Variáveis


| Variável | Significado                      |
|----------|----------------------------------|
| C        | Carro presente (1 = sim, 0 = não)|
| P        | Pagamento efetuado (1 = sim, 0 = não)|
| S        | Cancela abre (1 = sim, 0 = não)  |

## Tabela Verdade

| C (Carro) | P (Pagamento) | S (Cancela abre) |
|:--------:|:-------------:|:----------------:|
|    0     |       0       |        0         |
|    0     |       1       |        0         |
|    1     |       0       |        0         |
|    1     |       1       |        1         |

## Expressão Canônica (Soma de Mintermos)

A saída S é 1 apenas na linha onde C = 1 e P = 1:

**S = C · P = 1**

## Explicação da Lógica

> A cancela **só será aberta** quando:
> - Um carro estiver presente (`C = 1`)
> - E o pagamento tiver sido realizado (`P = 1`)

## Circuito Lógico

Componentes:
- 2 entradas (Switches)
- 1 Porta AND
- 1 saída (LED)
  
```text
C ───┐
├── AND ─── S
P ───┘
```
