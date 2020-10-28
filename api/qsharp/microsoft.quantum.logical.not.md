---
uid: Microsoft.Quantum.Logical.Not
title: Not, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709867"
---
# <a name="not-function"></a>Not, функция

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


Возвращает логическое отрицание значения.

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a>Входные данные

### <a name="value--bool"></a>значение: [bool](xref:microsoft.quantum.lang-ref.bool)

Значение, которое необходимо инвертировать.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и только если `value` имеет значение `false` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let x = not value;
let x = Not(value);
```