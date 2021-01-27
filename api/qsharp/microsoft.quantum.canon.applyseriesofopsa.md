---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Операция Апплисериесофопса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: 052cb52d4ee6500e60043ab7f808497058924afe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844663"
---
# <a name="applyseriesofopsa-operation"></a>Операция Апплисериесофопса

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет список Ops и их целевых объектов последовательно в массиве. (Прилегающий)

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="listofops--t--unit--is-adj"></a>Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []

Список операций, каждый из которых принимает массив «t» для применения. Они применяются последовательно, сначала по нижнему индексу.
Каждый должен иметь смежный функтор


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих индексы для использования.


### <a name="register--t"></a>Register: не []

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="example"></a>Пример

Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубита (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопса (Ops, indices, Кубитаррай);

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплйопрепеатедлйовер](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)