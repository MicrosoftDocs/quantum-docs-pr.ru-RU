---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Операция Мултипляндаддбимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 169326879919b5b72d600c33d624776b720cc6bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222598"
---
# <a name="multiplyandaddbymodularinteger-operation"></a>Операция Мултипляндаддбимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет модульные целочисленные константы умножения и добавления в регистре кубит.

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Реализует карту $ $ \бегин{алигн} \кет{КС} \кет{б} \мапсто \кет{КС} \кет{(b + a \кдот x) \операторнаме{мод} N} \енд{алигн} $ $ для данного модуля $N $, постоянный множитель $a $ и слагаемому $y $.

## <a name="input"></a>Входные данные

### <a name="constmultiplier--int"></a>Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)

Целое число $a $, добавляемое к каждой метке состояния базы данных.


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Модуль $N $, для которого выполняется сложение и умножение, относительно.


### <a name="multiplier--littleendian"></a>множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .


### <a name="summand--littleendian"></a>слагаемому: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

- Схема канала и описание см. на рис. 6 на [стр. 7 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)
- Эта операция соответствует КМУЛТ (a) MOD (N) в [арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Мултипляндаддфасебимодуларинтежер](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)