---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a56d28e34938729a8e4ffda5f870e0b6a25be017
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857516"
---
# <a name="fraction-user-defined-type"></a>Определяемый пользователем тип дроби

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет рациональное число в форме `p/q` . Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="numerator--int"></a>Числитель: [int](xref:microsoft.quantum.lang-ref.int)

Числитель дробной части.
### <a name="denominator--int"></a>Знаменатель: [int](xref:microsoft.quantum.lang-ref.int)

Знаменатель дроби/