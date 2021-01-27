---
uid: Microsoft.Quantum.Bitwise.Or
title: Или, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845269"
---
# <a name="or-function"></a>Или, функция

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает побитовое или для двух целых чисел.
При этом выполняются те же вычисления, что и у встроенного `|||` оператора.

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)




### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Пример

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a>Remarks

См. раздел [C# | Оператор](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) для получения дополнительных сведений.