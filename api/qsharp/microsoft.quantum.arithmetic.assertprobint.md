---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Операция Ассертпробинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843402"
---
# <a name="assertprobint-operation"></a>Операция Ассертпробинт

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Пример

Предположим, что `qubits` регистр кодирует 3-кубитное состояние такта $ \кет{\пси} = \ sqrt {1/8} \ Сисакет {0} + \ sqrt {7/8} \ Сисакет {6} $ в формате с прямым порядком байтов.
Это означает, что число состояний $ \кет {0} \екуив\кет {0} \кет {0} \кет {0} $ и $ \кет {6} \екуив\кет {0} \кет {1} \кет {1} $. Затем выполняются следующие утверждения:

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```