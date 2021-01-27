---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 353442a4245a9e20bb1e4c46d2e8a84d4c9534b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857772"
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

## <a name="example"></a>Пример

Следующие два распределения идентичны:

```qsharp
let dist1 = ContinuousUniformDistribution(1.0, 2.0);
let dist2 = TransformedContinuousDistribution(
    PlusD(1.0, _),
    ContinuousUniformDistribution(0.0, 1.0)
);
```