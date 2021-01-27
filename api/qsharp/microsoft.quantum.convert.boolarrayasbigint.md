---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Функция Буларрайасбигинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 220a733b94fd62cef21ab13e1cb3d3f973861506
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834417"
---
# <a name="boolarrayasbigint-function"></a>Функция Буларрайасбигинт

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Преобразует заданный массив логических значений в эквивалентное большое целое число.
Элемент 0 массива является наименее значащим битом длинного целого числа.

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a>Входные данные

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)[]





## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе [конструктор C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .