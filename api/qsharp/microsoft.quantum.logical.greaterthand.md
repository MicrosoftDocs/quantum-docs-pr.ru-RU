---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: Функция Греатерсанд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: c23d85cf513bb6d37e67260eeeb3b81b42e6771a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198033"
---
# <a name="greaterthand-function"></a>Функция Греатерсанд

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если число больше, чем другое число.

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--double"></a>ответ. [Double](xref:microsoft.quantum.lang-ref.double)

Первое сравниваемое значение.


### <a name="b--double"></a>б: [двойной](xref:microsoft.quantum.lang-ref.double)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` только в случае, если `a` строго больше `b` .

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```