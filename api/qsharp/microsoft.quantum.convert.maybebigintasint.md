---
uid: Microsoft.Quantum.Convert.MaybeBigIntAsInt
title: Функция Майбебигинтасинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: MaybeBigIntAsInt
qsharp.summary: Converts a given big integer to an equivalent integer, if possible. The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.
ms.openlocfilehash: b91912f6f669afad888e71174fef6e2e6f8e7156
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713437"
---
# <a name="maybebigintasint-function"></a>Функция Майбебигинтасинт

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


Преобразует заданное большое целое число в эквивалентное целое число, если это возможно.
Функция возвращает пару результирующего целого числа и логический флаг, который имеет значение true, только если преобразование возможно.

```qsharp
function MaybeBigIntAsInt (a : BigInt) : (Int, Bool)
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--intbool"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool))



## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе [конструктор C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .