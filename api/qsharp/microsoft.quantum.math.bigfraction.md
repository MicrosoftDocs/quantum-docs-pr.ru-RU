---
uid: Microsoft.Quantum.Math.BigFraction
title: Определяемый пользователем тип Бигфрактион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732768"
---
# <a name="bigfraction-user-defined-type"></a>Определяемый пользователем тип Бигфрактион

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Представляет рациональное число в форме `p/q` . Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Именованные элементы

### <a name="numerator--bigint"></a>Числитель: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Числитель дробной части.
### <a name="denominator--bigint"></a>Знаменатель: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Знаменатель дроби/