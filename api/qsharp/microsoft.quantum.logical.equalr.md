---
uid: Microsoft.Quantum.Logical.EqualR
title: Функция Equals
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d68b2f1a26bf318400d3c88b37d9aabcc38cbdfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198012"
---
# <a name="equalr-function"></a>Функция Equals

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если два входных значения равны.

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--__invalidresult__"></a>ответ. __Недопустимый <Result>__

Первое сравниваемое значение.


### <a name="b--__invalidresult__"></a>б: __недопустимо <Result>__

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` равно `b` .

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```