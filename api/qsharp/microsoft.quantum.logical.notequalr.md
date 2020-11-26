---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Функция Нотекуалр
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197200"
---
# <a name="notequalr-function"></a>Функция Нотекуалр

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```