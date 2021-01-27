---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Операция Препарекубит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: e6a88ccf4c01b2f0a7344e3823b2748790cf9650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854339"
---
# <a name="preparequbit-operation"></a>Операция Препарекубит

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Препарекубит является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate>.

Подготавливает кубит в еиженстате + 1 ( `Zero` ) для данного оператора Паули.
Если указан оператор Identity, кубит подготавливается в максимально смешанном состоянии.

Если кубит изначально находится в состоянии $ \кет {0} $, эта операция подготавливает кубит в еиженстате $ + $1 для данного оператора Паули или, для `PauliI` , в максимально смешанном состоянии (см <xref:microsoft.quantum.preparation.preparesinglequbitidentity> .).

Если кубит находится в состоянии, отличном от $ \кет {0} $, эта операция применяет следующие шлюзы: $H $ for `PauliX` , $HS $ для `PauliY` , $I $ for `PauliZ` и <xref:microsoft.quantum.preparation.preparesinglequbitidentity> для `PauliI` .

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="basis--pauli"></a>Базис: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор Паули $P $.


### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, который необходимо подготовить.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

