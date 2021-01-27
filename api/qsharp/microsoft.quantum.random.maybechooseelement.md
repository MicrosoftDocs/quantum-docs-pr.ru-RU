---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Операция Майбечусилемент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856114"
---
# <a name="maybechooseelement-operation"></a>Операция Майбечусилемент

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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



## <a name="example"></a>Пример

Следующий фрагмент Q # выбирает элемент случайным образом из массива:

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```