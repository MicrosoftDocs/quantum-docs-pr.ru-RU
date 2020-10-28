---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Функция Нотекуалр
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709797"
---
# <a name="notequalr-function"></a>Функция Нотекуалр

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


Возвращает значение true только в том случае, если два входных значения не равны.

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--__invalidresult__"></a>ответ. __Недопустимый <Result>__

Первое сравниваемое значение.


### <a name="b--__invalidresult__"></a>б: __недопустимо <Result>__

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` не равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```