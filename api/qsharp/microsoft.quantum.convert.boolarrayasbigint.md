---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Функция Буларрайасбигинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 75656ba188a1b822eb42e98412365bf5873bf46e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713619"
---
# <a name="boolarrayasbigint-function"></a>Функция Буларрайасбигинт

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


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