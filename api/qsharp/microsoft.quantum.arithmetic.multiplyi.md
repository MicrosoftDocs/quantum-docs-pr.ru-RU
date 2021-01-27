---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Операция Мултипли
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 8615d0d5100c26f86264ceaecadb7783563216a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843029"
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



## <a name="remarks"></a>Remarks

Использует стандартный подход Shift и-Add для реализации умножения.
Управляемая версия была улучшена путем копирования $x _i $ в анЦилла кубит, на Кубитс элемента управления, а затем управления добавлением анЦилла кубит.