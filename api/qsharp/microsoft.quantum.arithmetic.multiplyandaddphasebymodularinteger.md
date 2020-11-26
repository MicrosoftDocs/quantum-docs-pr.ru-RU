---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Операция Мултипляндаддфасебимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: 1ca20b525d2a76e554d5a2e8d4f40060b5ef51cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223873"
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



## <a name="remarks"></a>Комментарии

Предполагается, что `phaseSummand` имеет наивысший бит, равный 0.
Также предполагается, что значение `phaseSummand` меньше $N $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Мултипляндаддбимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)