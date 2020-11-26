---
uid: Microsoft.Quantum.Math.BigFraction
title: Определяемый пользователем тип Бигфрактион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211089"
---
# <a name="bigfraction-user-defined-type"></a>Определяемый пользователем тип Бигфрактион

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет рациональное число в форме `p/q` . Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Именованные элементы

### <a name="numerator--bigint"></a>Числитель: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Числитель дробной части.
### <a name="denominator--bigint"></a>Знаменатель: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Знаменатель дроби/