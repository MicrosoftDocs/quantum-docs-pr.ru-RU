---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderD
title: Операция Рипплекарряддерд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderD
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: b87c8f25acc8854d5e8d28f58cfc99dffb92a973
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222122"
---
# <a name="ripplecarryadderd-operation"></a>Операция Рипплекарряддерд

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Обратимое выполнение — добавление двух целых чисел.
Учитывая два $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` и `ys` , и кубит, операция вычисляет сумму двух целых чисел, в которых $n $ наименьшие значащие биты результата, `ys` а бит выполнения — ксоред кубит `carry` .

```qsharp
operation RippleCarryAdderD (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения $n $ наименьших значащих разрядов суммы.


### <a name="carry--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, ксоред с наиболее значащим битом суммы.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.

## <a name="references"></a>Ссылки

- Томас G. Драпер: "Добавление на тактовый компьютер", 2000.
  https://arxiv.org/abs/quant-ph/0008033