---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192967"
---
# <a name="drawrandombool-operation"></a>Операция Драврандомбул

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Учитывая вероятность успеха, возвращает одну пробную версию Бернулли, которая имеет значение true с заданной вероятностью.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="successprobability--double"></a>Сукцесспробабилити: [Double](xref:microsoft.quantum.lang-ref.double)

Вероятность, с которой `true` должно возвращаться значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` с вероятностью `successProbability` и `false` с вероятностью `1.0 - successProbability` .