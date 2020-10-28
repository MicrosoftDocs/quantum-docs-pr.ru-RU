---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Операция Инкрементфасебимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731473"
---
# <a name="incrementphasebymodularinteger-operation"></a>Операция Инкрементфасебимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Выполняет модульное увеличение регистра кубит с помощью целочисленной константы.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a>Описание

Отметим, `increment` что $a $, `modulus` $N $ и целое число, закодированные `target` $y $.
Затем операция выполняет следующее преобразование: \бегин{алигн} \кет{и} \мапсто \кет{(y + a) \операторнаме{мод} N} \енд{алигн} целые числа в Кфт кодируются в формате с прямым порядком байтов.

## <a name="input"></a>Входные данные

### <a name="increment--int"></a>приращение: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленное приращение $a $, добавляемое в $y $.


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Integer $N $, МОДС $y + a $.


### <a name="target--phaselittleendian"></a>Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Целое число $y $ в формате с прямым порядком байтов в кодировке, который `increment` $a $ добавляется в.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что `target` имеет наивысший бит, равный 0.
Также предполагается, что значение целевого объекта меньше $N $.

Схема канала и описание см. на рис. 5 на [стр. 5 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Инкрементбимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)