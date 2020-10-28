---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710945"
---
# <a name="transformedcontinuousdistribution-function"></a>Функция Трансформедконтинуаусдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


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