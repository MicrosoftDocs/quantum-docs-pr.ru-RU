---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854570"
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