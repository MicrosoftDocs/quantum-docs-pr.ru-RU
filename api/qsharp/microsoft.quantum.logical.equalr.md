---
uid: Microsoft.Quantum.Logical.EqualR
title: Функция Equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710035"
---
# <a name="equalr-function"></a>Функция Equals

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```