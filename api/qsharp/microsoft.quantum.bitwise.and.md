---
uid: Microsoft.Quantum.Bitwise.And
title: Функции и
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: And
qsharp.summary: Returns the bitwise AND of two integers. This performs the same computation as the built-in `&&&` operator.
ms.openlocfilehash: 56eae4ef222a6593fd97966a9af21d559f613bc3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842168"
---
# <a name="and-function"></a>Функции и

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает побитовое и для двух целых чисел.
При этом выполняются те же вычисления, что и у встроенного `&&&` оператора.

```qsharp
function And (a : Int, b : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)




### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Пример

```qsharp
let a = 248;       //                11111000₂
let b = 63;        //                00111111₂
let x = And(a, b); // x : Int = 56 = 00111000₂.
```

## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе [ &amp; оператор C#](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/and-operator) (двоичный).