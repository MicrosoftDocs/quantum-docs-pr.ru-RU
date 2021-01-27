---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Операция Мултипляндаддфасебимодуларинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: b1214acc2cafc3fede9fcb6663a435c0b1d2cf4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843062"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a>Операция Мултипляндаддфасебимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


То же, что и Мултипляндаддбимодуларинтежер, но предполагает, что слагаемому кодирует целые числа в Кфт.

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="constmultiplier--int"></a>Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)

Целое число $a $, добавляемое к каждой метке состояния базы данных.


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Модуль $N $, для которого выполняется сложение и умножение, относительно.


### <a name="multiplier--littleendian"></a>множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .


### <a name="phasesummand--phaselittleendian"></a>Фасесумманд: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что `phaseSummand` имеет наивысший бит, равный 0.
Также предполагается, что значение `phaseSummand` меньше $N $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Мултипляндаддбимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)