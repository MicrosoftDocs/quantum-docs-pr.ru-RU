---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: Функция Континуедфрактионконвержентл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c10fcbbe63d3d4c7d6c56196768c1062be1ca350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210936"
---
# <a name="continuedfractionconvergentl-function"></a>Функция Континуедфрактионконвержентл

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a>Входные данные

### <a name="fraction--bigfraction"></a>Дробь: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)




### <a name="denominatorbound--bigint"></a>Деноминаторбаунд: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigfraction"></a>Выходные данные: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)

Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`