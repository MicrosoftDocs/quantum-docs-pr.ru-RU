---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Операция Апплисериесофопска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850868"
---
# <a name="applyseriesofopsca-operation"></a>Операция Апплисериесофопска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет список Ops и их целевых объектов последовательно в массиве. (Смежное + управление)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="listofops--t--unit--is-adj--ctl"></a>Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"

Список операций, каждый из которых принимает массив «t» для применения. Они применяются последовательно, сначала по нижнему индексу.
Каждый из них должен иметь одновременно соседний и контролируемый функтор.


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих индексы для использования.


### <a name="register--t"></a>Register: не []

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="example"></a>Пример

Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубитка (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопска (Ops, indices, Кубитаррай);

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплйопрепеатедлйовер](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)