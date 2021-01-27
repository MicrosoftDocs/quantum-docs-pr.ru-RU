---
uid: Microsoft.Quantum.Logical.Not
title: Not, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849078"
---
# <a name="not-function"></a>Not, функция

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

```qsharp
let x = not value;
let x = Not(value);
```