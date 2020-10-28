---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Операция Ассертпробинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731680"
---
# <a name="assertprobint-operation"></a>Операция Ассертпробинт

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Утверждает, что вероятность определенного состояния регистра такта имеет ожидаемое значение.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>Описание

Учитывая $n $-кубит State $ \кет{\пси} = \сум ^ {2 ^ n-1} _ {j = 0} \ alpha_j \кет{ж} $, утверждает, что вероятность $ | \ alpha_j | ^ 2 $ из состояния $ \кет{ж} $, индексируемого $j $, имеет ожидаемое значение.

## <a name="input"></a>Входные данные

### <a name="stateindex--int"></a>Статеиндекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс $j $ из состояния $ \кет{ж} $, представленного `LittleEndian` регистром.


### <a name="expected--double"></a>ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)

Ожидаемое значение $ | \ alpha_j | ^ 2 $.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр кубит, в котором хранится $ \кет{\пси} $ в формате с прямым порядком байтов.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Абсолютная погрешность разности между фактическим и ожидаемым.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

