---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Функция Континуедфрактионконверженти
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: 2322e005a5afb73d9719eb65d9ebf50740f1c9fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732752"
---
# <a name="continuedfractionconvergenti-function"></a>Функция Континуедфрактионконверженти

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a>Входные данные

### <a name="fraction--fraction"></a>Дробь: [дробь](xref:Microsoft.Quantum.Math.Fraction)




### <a name="denominatorbound--int"></a>Деноминаторбаунд: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--fraction"></a>Выходные данные: [дробь](xref:Microsoft.Quantum.Math.Fraction)

Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`