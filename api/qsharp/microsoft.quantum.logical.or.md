---
uid: Microsoft.Quantum.Logical.Or
title: Или, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848467"
---
# <a name="or-function"></a>Или, функция

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает логическое сложение двух значений.

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bool"></a>ответ. [bool](xref:microsoft.quantum.lang-ref.bool)

Первое значение, которое необходимо считать.


### <a name="b--bool"></a>б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение

Второе значение, которое необходимо считать.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, и только в том случае `a` , если имеет значение или `b` `true` .

## <a name="remarks"></a>Remarks

В отличие от `or` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.

Ниже приведены эквивалентные действия для сокращенного поведения.

```qsharp
let x = a or b;
let x = Or(a, b);
```