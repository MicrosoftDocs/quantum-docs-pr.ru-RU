---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853696"
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

## <a name="example"></a>Пример

Следующие примеры кода Q # переворачиваются с смещенной монет:

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```