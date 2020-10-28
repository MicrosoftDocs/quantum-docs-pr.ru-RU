---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733401"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Определяемый пользователем тип Унивариатеоптимизатионресулт

Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)

Пакеты [](https://nuget.org/packages/)


Представляет результат оптимизации функции унивариате.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Именованные элементы

### <a name="coordinate--double"></a>Координата: [Двойное](xref:microsoft.quantum.lang-ref.double)

Входные данные, для которых была обнаружена оптимальная.
### <a name="value--double"></a>Значение: [Double](xref:microsoft.quantum.lang-ref.double)

Значение, возвращаемое функцией в своей оптимальной области.