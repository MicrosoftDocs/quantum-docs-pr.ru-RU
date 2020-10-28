---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Операция Инкрементбимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731504"
---
# <a name="incrementbymodularinteger-operation"></a>Операция Инкрементбимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Выполняет модульное увеличение регистра кубит с помощью целочисленной константы.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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



## <a name="remarks"></a>Remarks

Предполагается, что начальное значение целевого объекта меньше $N $, а шаг приращения $a $ меньше $N $.
Обратите внимание, что <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> реализует ту же операцию на `PhaseLittleEndian` основе.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Инкрементфасебимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)