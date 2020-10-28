---
uid: Microsoft.Quantum.Logical.EqualI
title: Функция Екуали
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 6b805e76217e033cb0135cf85bd8f37a3eb8636a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710050"
---
# <a name="equali-function"></a>Функция Екуали

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


Возвращает значение true только в том случае, если два входных значения равны.

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)

Первое сравниваемое значение.


### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```