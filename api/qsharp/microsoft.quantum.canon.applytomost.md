---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Операция Апплитомост
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850596"
---
# <a name="applytomost-operation"></a>Операция Апплитомост

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию ко всему элементу массива, кроме последнего.

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будут применены все, кроме последнего `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="example"></a>Пример

Следующие фрагменты кода Q # эквивалентны:

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитомоста](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [Microsoft. тактов. Canon. Апплитомостк](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [Microsoft. тактов. Canon. Апплитомостка](xref:Microsoft.Quantum.Canon.ApplyToMostCA)