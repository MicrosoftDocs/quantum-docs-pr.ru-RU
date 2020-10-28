---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Функция Лесссанорекуалл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 333b76fc4885104e107dd25003a4e0dd5a9dd4af
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709923"
---
# <a name="lessthanorequall-function"></a>Функция Лесссанорекуалл

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


Возвращает значение true только в том случае, если число меньше или равно другому числу.

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Первое сравниваемое значение.


### <a name="b--bigint"></a>б: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` только в случае, если `a` меньше или равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```