---
uid: Microsoft.Quantum.Logical.Or
title: Или, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 7093d908696a8cfda6b5ef648f9dfafcfac97144
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197132"
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

## <a name="remarks"></a>Комментарии

В отличие от `or` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.

Ниже приведены эквивалентные действия для сокращенного поведения.

```Q#
let x = a or b;
let x = Or(a, b);
```