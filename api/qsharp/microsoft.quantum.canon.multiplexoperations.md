---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Операция Мултиплексоператионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 267c9c2858090ebe024fd387938e8bd2f8c76867
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715832"
---
# <a name="multiplexoperations-operation"></a>Операция Мултиплексоператионс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет массив операций, управляемых массивом числовых состояний.

Это значит, что применяет операцию с множественным контролем, $U $, которая применяет единое $V _j $ при управлении с $n $-кубит номер состояния $ \кет{ж} $.

$U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a>Входные данные

### <a name="unitaries--t--unit-adj--ctl"></a>унитариес: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []

Массив операций до $2 ^ n $ от единой операции. Операция $j $ TH индексируется по числу состояния $ \кет{ж} $, закодированному в формате с прямым порядком байтов.


### <a name="index--littleendian"></a>Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.


### <a name="target--t"></a>Целевой объект: 'T

Универсальный кубит регистр, который $V _j $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

`coefficients` будут заполнены элементами Identity, если указано меньше $2 ^ n $. В этой реализации используется $n-$1 вспомогательная Кубитс.

## <a name="references"></a>Ссылки

- К первому моделированию такта с увеличением такта, Дмитрий Маслов, Вьетнам Юнсеонг, Нил J. Росс (, Юань SU https://arxiv.org/abs/1711.10980