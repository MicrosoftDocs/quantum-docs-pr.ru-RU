---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Операция Мултипли
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 96922f0147788b37cc9bace5154288a722d4ba95
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222513"
---
# <a name="multiplyi-operation"></a>Операция Мултипли

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Умножьте целое число `xs` на целое `ys` и сохраните результат в `result` , который должен быть равен нулю изначально.

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bit множимое (Литтлиндиан)


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-разрядный множитель (Литтлиндиан)


### <a name="result--littleendian"></a>результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2N $-bit Result (Литтлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Использует стандартный подход Shift и-Add для реализации умножения.
Управляемая версия была улучшена путем копирования $x _i $ в анЦилла кубит, на Кубитс элемента управления, а затем управления добавлением анЦилла кубит.