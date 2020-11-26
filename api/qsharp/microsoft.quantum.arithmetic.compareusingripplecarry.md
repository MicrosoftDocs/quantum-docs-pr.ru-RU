---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Операция Компареусингрипплекарри
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223465"
---
# <a name="compareusingripplecarry-operation"></a>Операция Компареусингрипплекарри

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Эта операция проверяет, имеет ли целое число, представленное регистром Кубитс, больше другого целого числа, применяя XOR результата к выходному кубит.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

При наличии двух целых чисел `x` и `y` хранении в регистрах кубит одинакового размера эта операция проверяет, соответствуют ли они `x > y` . Если значение равно true, 1 Ксоред в выходной кубит. В противном случае 0 Ксоред в выходной кубит.
Иными словами, эта операция может быть представлена единой $ $ \бегин{алигн} У\кет {x} \ Сисакет {y} \ Сисакет {z} = \кет{КС}\кет{и}\кет{з\оплус (x>y)}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="x--littleendian"></a>x: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Первое число для сравнения, хранимое в `LittleEndian` формате в регистре кубит.


### <a name="y--littleendian"></a>Да: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Второе число для сравнения, сохраненное в `LittleEndian` формате в регистре кубит.


### <a name="output--qubit"></a>выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, в котором хранится результат сравнения $x>y $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Новый такт Ripple — Добавление Андрея A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон https://arxiv.org/abs/quant-ph/0410184