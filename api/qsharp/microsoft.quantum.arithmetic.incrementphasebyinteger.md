---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Операция Инкрементфасебинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843143"
---
# <a name="incrementphasebyinteger-operation"></a>Операция Инкрементфасебинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Увеличивает значение регистра неподписанного такта на классическое целое число с использованием ротаций фазы.

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Предположим, что `target` кодирует целое число без знака $x $ в кодировке с прямым порядком байтов и `increment` равно $a $.
Затем эта операция реализует единую $ \кет{КС} \мапсто \кет{КС + a} $, где сложение выполняется по модулю $2 ^ n $, где $n = \Тексттт{ленгс (Target!)} $.

## <a name="input"></a>Входные данные

### <a name="increment--int"></a>приращение: [int](xref:microsoft.quantum.lang-ref.int)

Целое число, на которое `target` увеличивается значение.


### <a name="target--phaselittleendian"></a>Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Тактовый регистр кодирует целое число без знака, используя обратную кодировку с прямым порядком байтов в двойном (Кфт) уровне.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Обратите внимание, что мы упростили канал, так как инкремент является классической константой, а не тактовой регистром.

См. рисунок на [ стр. 6 из арксив: Куант-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) для схемы канала и объяснения.

## <a name="references"></a>Ссылки

- [*Томас G. Драпер*, арксив: Куант-pH/0008033](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Инкрементбинтежер](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)