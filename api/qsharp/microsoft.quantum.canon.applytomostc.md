---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Операция Апплитомостк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 14de9f367aa7d19f64f13186d402239ae1fef3c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850559"
---
# <a name="applytomostc-operation"></a>Операция Апплитомостк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию ко всему элементу массива, кроме последнего.

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-ctl"></a>Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будут применены все, кроме последнего `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитомост](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [Microsoft. тактов. Canon. Апплитомоста](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [Microsoft. тактов. Canon. Апплитомостка](xref:Microsoft.Quantum.Canon.ApplyToMostCA)