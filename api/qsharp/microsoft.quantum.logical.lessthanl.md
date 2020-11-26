---
uid: Microsoft.Quantum.Logical.LessThanL
title: Функция Лесссанл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 9a0678569596ac188c87c3944f3759783fcc77ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197727"
---
# <a name="lessthanl-function"></a>Функция Лесссанл

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если число меньше, чем другое число.

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Первое сравниваемое значение.


### <a name="b--bigint"></a>б: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` является строго меньшим `b` .

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```