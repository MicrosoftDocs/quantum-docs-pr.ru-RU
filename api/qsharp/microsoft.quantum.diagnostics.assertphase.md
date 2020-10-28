---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Операция Ассертфасе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712948"
---
# <a name="assertphase-operation"></a>Операция Ассертфасе

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждает, что фаза равного пресостояния перестановки имеет ожидаемое значение.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>Описание

Эта операция подтверждает, что фаза $ \фи $ состояния такта, которая может быть выражена как $ \фрак{е ^ {i t}} {\скрт {2} } (e ^ {и\фи} \ Сисакет {0} + e ^ {-и\фи} \ Сисакет {1} ) $ для некоторых произвольных реальных $t $ имеет ожидаемое значение.

## <a name="input"></a>Входные данные

### <a name="expected--double"></a>ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)

Ожидаемое значение $ \фи \ин (-\пи, \пи] $.


### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, в котором хранится ожидаемое состояние.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Абсолютная погрешность разности между фактическим и ожидаемым.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

