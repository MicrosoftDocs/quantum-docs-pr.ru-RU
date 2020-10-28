---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Операция Апплитоелемент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5c321d95c9b79bc50827c2b50c406b164e143dc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717511"
---
# <a name="applytoelement-operation"></a>Операция Апплитоелемент

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию к заданному элементу массива.

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

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

- [Microsoft. тактов. Canon. Апплитоелементк](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. тактов. Canon. Апплитоелемента](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [Microsoft. тактов. Canon. Апплитоелементка](xref:Microsoft.Quantum.Canon.ApplyToElementCA)