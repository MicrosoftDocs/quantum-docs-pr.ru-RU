---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Операция Апплитоелементка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 599a8afe1ab97b0ab0d6621cabd7707faaeddda3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717442"
---
# <a name="applytoelementca-operation"></a>Операция Апплитоелементка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию к заданному элементу массива.

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj--ctl"></a>Op: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Операция, которую необходимо применить.


### <a name="index--int"></a>Индекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс в массиве целевых объектов.


### <a name="targets--t"></a>targets: 'T []

Массив возможных целевых объектов для `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоелемент](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [Microsoft. тактов. Canon. Апплитоелементк](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. тактов. Canon. Апплитоелемента](xref:Microsoft.Quantum.Canon.ApplyToElementA)