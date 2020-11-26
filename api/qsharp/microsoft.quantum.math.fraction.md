---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210681"
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