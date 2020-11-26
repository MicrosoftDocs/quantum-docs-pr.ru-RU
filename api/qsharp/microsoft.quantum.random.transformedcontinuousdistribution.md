---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226270"
---
# <a name="transformedcontinuousdistribution-function"></a>Функция Трансформедконтинуаусдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


При наличии непрерывного распределения возвращает новое распределение, которое преобразует оригинал с помощью заданной функции.

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Входные данные

### <a name="transform--double---double"></a>Преобразование: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)

Функция, которая преобразует вариатес исходного распределения в преобразованное распределение.


### <a name="distribution--continuousdistribution"></a>распространение: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Исходное распределение для преобразования.



## <a name="output--continuousdistribution"></a>Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Новое распределение, относящееся к `distribution` преобразованию, заданному параметром `transform` .