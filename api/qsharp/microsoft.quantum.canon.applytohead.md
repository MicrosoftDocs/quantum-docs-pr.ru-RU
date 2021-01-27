---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Операция Апплитохеад
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e627b467e9354e774c2ead8b89ddd3ff3a42ef7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841335"
---
# <a name="applytohead-operation"></a>Операция Апплитохеад

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первому элементу массива.

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будет применен первый из них `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="example"></a>Пример

Следующие фрагменты кода Q # эквивалентны:

```qsharp
ApplyToHead(H, register);
H(Head(register));
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитохеада](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [Microsoft. тактов. Canon. Апплитохеадк](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [Microsoft. тактов. Canon. Апплитохеадка](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)