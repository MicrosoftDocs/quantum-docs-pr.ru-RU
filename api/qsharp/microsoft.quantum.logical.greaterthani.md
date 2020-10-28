---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Функция Греатерсани
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: ffd00d8086654a2d783a351fe254fb2ee35b9184
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709980"
---
# <a name="greaterthani-function"></a>Функция Греатерсани

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


Возвращает значение true только в том случае, если число больше, чем другое число.

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)

Первое сравниваемое значение.


### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` только в случае, если `a` строго больше `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```