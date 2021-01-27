---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Операция Ассертфасе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830082"
---
# <a name="assertphase-operation"></a>Операция Ассертфасе

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Пример

Следующее утверждение выполнено: `qubit` находится в состоянии $ \кет{\пси} = e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {0} + e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {1} $;

- `AssertPhase(0.0,qubit,10e-10);`

`qubit` находится в состоянии $ \кет{\пси} = e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {0} + e ^ {-i 0,5} \ sqrt {1/2} \ Сисакет {1} $;

- `AssertPhase(0.5,qubit,10e-10);`

`qubit` находится в состоянии $ \кет{\пси} = e ^ {-i 2.2} \ корень {1/2} \ Сисакет {0} + e ^ {i 0,2} \ sqrt {1/2} \ Сисакет {1} $;

- `AssertPhase(-1.2,qubit,10e-10);`