---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Операция Препарепаулиеиженстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854352"
---
# <a name="preparepaulieigenstate-operation"></a>Операция Препарепаулиеиженстате

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Подготавливает кубит в положительном еиженстатее данного оператора Паули.
Если указан оператор Identity, кубит подготавливается в максимально смешанном состоянии.

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a>Описание

Если кубит изначально находится в состоянии $ \кет {0} $, эта операция подготавливает кубит в еиженстате $ + $1 для данного оператора Паули или, для `PauliI` , в максимально смешанном состоянии (см <xref:microsoft.quantum.preparation.preparesinglequbitidentity> .).

Если кубит находится в состоянии, отличном от $ \кет {0} $, эта операция применяет следующие шлюзы: $H $ for `PauliX` , $HS $ для `PauliY` , $I $ for `PauliZ` и <xref:microsoft.quantum.preparation.preparesinglequbitidentity> для `PauliI` .

## <a name="input"></a>Входные данные

### <a name="basis--pauli"></a>Базис: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор Паули $P $.


### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, который необходимо подготовить.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

Чтобы подготовить кубит в состоянии $ \кет{+} $, сделайте следующее:

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```