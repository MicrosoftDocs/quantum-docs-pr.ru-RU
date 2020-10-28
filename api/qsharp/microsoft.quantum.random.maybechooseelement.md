---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Операция Майбечусилемент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732169"
---
# <a name="maybechooseelement-operation"></a>Операция Майбечусилемент

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


При наличии массива данных и распределения по индексам пытается выбрать элемент в случайном порядке.

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a>Входные данные

### <a name="data--t"></a>данные: 'T []

Массив, из которого должен быть выбран элемент.


### <a name="indexdistribution--discretedistribution"></a>Индексдистрибутион: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Распределение по индексам `data` .



## <a name="output--boolt"></a>Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

