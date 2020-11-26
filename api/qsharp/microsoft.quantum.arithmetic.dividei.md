---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Операция Дивидеи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 4cff191e1f9d42659768b4059e477f1a07948ba1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223312"
---
# <a name="dividei-operation"></a>Операция Дивидеи

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Делит два целочисленных целых числа.

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

`xs` будет содержать остаток `xs - floor(xs/ys) * ys` и `result` будет содержать `floor(xs/ys)` .

## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bit делимое будет заменено остатком.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-разрядный делитель


### <a name="result--littleendian"></a>результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-разрядный результат, должен находиться в состоянии $ \кет {0} $ изначально и заменяться результатом целочисленного деления.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Использует стандартный подход с сдвигом и вычитанием для реализации деления.
Контролируемая версия является специализированной, поэтому вычитание не требует дополнительных элементов управления.