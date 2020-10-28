---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Функция Локалунивариатеминимум
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: 3b09af88bbed20a392768d005e5e9567b3bb7022
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711016"
---
# <a name="localunivariateminimum-function"></a>Функция Локалунивариатеминимум

Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)

Пакеты [](https://nuget.org/packages/)


Возвращает локальное минимальное значение для функции унивариате через ограниченный интервал при помощи золотого интервала поиска.

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a>Входные данные

### <a name="fn--double---double"></a>FN: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)

Функция унивариате для сворачивания.


### <a name="bounds--doubledouble"></a>границы: ([Двойное](xref:microsoft.quantum.lang-ref.double),[двойной](xref:microsoft.quantum.lang-ref.double))

Интервал, в течение которого должно быть найдено локальное минимальное значение.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Точность входных данных функции, которая будет допускаться.
Поиск локальной Оптима будет продолжен до тех пор, пока интервал не уменьшится по ширине.



## <a name="output--univariateoptimizationresult"></a>Выходные данные: [унивариатеоптимизатионресулт](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)

Локальная Оптима заданной функции, расположенная в пределах заданных границ.