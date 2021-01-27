---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Операция Апплисериесофопск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844648"
---
# <a name="applyseriesofopsc-operation"></a>Операция Апплисериесофопск

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет список Ops и их целевых объектов последовательно в массиве. Управляет

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="listofops--t--unit--is-ctl"></a>Листофопс: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL []

Список операций, каждый из которых принимает массив «t» для применения. Они применяются последовательно, сначала по нижнему индексу.
Каждый из них должен иметь управляемый функтор


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих индексы для использования.


### <a name="register--t"></a>Register: не []

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="example"></a>Пример

Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубитк (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопск (Ops, indices, Кубитаррай);

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплйопрепеатедлйовер](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)