---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Операция Инкрементбимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222955"
---
# <a name="incrementbymodularinteger-operation"></a>Операция Инкрементбимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет модульное увеличение регистра кубит с помощью целочисленной константы.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Отметим, `increment` что $a $, `modulus` $N $ и целое число, закодированные `target` $y $.
Затем операция выполняет следующее преобразование: \бегин{алигн} \кет{и} \мапсто \кет{(y + a) \операторнаме{мод} N} \енд{алигн} целые числа кодируются в формате с прямым порядком байтов.

## <a name="input"></a>Входные данные

### <a name="increment--int"></a>приращение: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленное приращение $a $, добавляемое в $y $.


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Integer $N $, МОДС $y + a $.


### <a name="target--littleendian"></a>Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Целочисленный $y $ в `LittleEndian` формате, `increment` к которому добавляется $a $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Предполагается, что начальное значение целевого объекта меньше $N $, а шаг приращения $a $ меньше $N $.
Обратите внимание, что <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> реализует ту же операцию на `PhaseLittleEndian` основе.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Инкрементфасебимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)