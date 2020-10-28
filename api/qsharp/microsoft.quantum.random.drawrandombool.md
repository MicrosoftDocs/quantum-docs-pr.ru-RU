---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730953"
---
# <a name="drawrandombool-operation"></a>Операция Драврандомбул

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


Учитывая вероятность успеха, возвращает одну пробную версию Бернулли, которая имеет значение true с заданной вероятностью.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="successprobability--double"></a>Сукцесспробабилити: [Double](xref:microsoft.quantum.lang-ref.double)

Вероятность, с которой `true` должно возвращаться значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` с вероятностью `successProbability` и `false` с вероятностью `1.0 - successProbability` .