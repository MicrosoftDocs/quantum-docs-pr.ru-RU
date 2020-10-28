---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733024"
---
# <a name="fraction-user-defined-type"></a>Определяемый пользователем тип дроби

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Представляет рациональное число в форме `p/q` . Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="numerator--int"></a>Числитель: [int](xref:microsoft.quantum.lang-ref.int)

Числитель дробной части.
### <a name="denominator--int"></a>Знаменатель: [int](xref:microsoft.quantum.lang-ref.int)

Знаменатель дроби/