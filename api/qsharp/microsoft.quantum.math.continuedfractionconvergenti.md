---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Функция Континуедфрактионконверженти
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c5316c13ce499da88c0d5c45b9d8c5e3a8c6162d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853861"
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