---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194038"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Определяемый пользователем тип Унивариатеоптимизатионресулт

Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет результат оптимизации функции унивариате.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Именованные элементы

### <a name="coordinate--double"></a>Координата: [Двойное](xref:microsoft.quantum.lang-ref.double)

Входные данные, для которых была обнаружена оптимальная.
### <a name="value--double"></a>Значение: [Double](xref:microsoft.quantum.lang-ref.double)

Значение, возвращаемое функцией в своей оптимальной области.