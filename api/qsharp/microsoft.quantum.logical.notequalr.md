---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Функция Нотекуалр
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 39601396a75d8c1b9193d4b8f34fa05466beff06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848502"
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

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let cond = a != b;
let cond = NotEqualR(a, b);
```