---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Операция Апплитоелемента
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 57d870c7fbd099212b13f75bd85e57c046280d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850772"
---
# <a name="applytoelementa-operation"></a>Операция Апплитоелемента

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к заданному элементу массива.

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a>Описание

При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-adj"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой

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
- [Microsoft. тактов. Canon. Апплитоелементка](xref:Microsoft.Quantum.Canon.ApplyToElementCA)