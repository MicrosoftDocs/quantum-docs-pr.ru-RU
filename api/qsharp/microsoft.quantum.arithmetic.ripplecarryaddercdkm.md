---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Операция Рипплекарряддеркдкм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: b08d8823fd539263205aca1ee15ee69adcb163b7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222105"
---
# <a name="ripplecarryaddercdkm-operation"></a>Операция Рипплекарряддеркдкм

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Обратимое выполнение — добавление двух целых чисел.

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Учитывая два $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` и `ys` , и кубит, операция вычисляет сумму двух целых чисел, в которых $n $ наименьшие значащие биты результата, `ys` а бит выполнения — ксоред кубит `carry` .

## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения n минимально значимых битов суммы.


### <a name="carry--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, ксоред с наиболее значащим битом суммы.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Эта операция имеет те же функциональные возможности, что и Рипплекарряддерд, но использует только один вспомогательный кубит вместо $n $.

## <a name="references"></a>Ссылки

- Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1