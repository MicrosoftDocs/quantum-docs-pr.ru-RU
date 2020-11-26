---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Функция Континуедфрактионконверженти
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: d37bf1c10899d06e798d29c68f88b06f2d5918a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195568"
---
# <a name="continuedfractionconvergenti-function"></a>Функция Континуедфрактионконверженти

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a>Входные данные

### <a name="fraction--fraction"></a>Дробь: [дробь](xref:Microsoft.Quantum.Math.Fraction)




### <a name="denominatorbound--int"></a>Деноминаторбаунд: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--fraction"></a>Выходные данные: [дробь](xref:Microsoft.Quantum.Math.Fraction)

Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`