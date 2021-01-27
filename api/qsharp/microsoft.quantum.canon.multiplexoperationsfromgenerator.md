---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Операция Мултиплексоператионсфромженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 59afa9d9a34fe74206118680940d243ed8b2496e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852495"
---
# <a name="multiplexoperationsfromgenerator-operation"></a>Операция Мултиплексоператионсфромженератор

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, управляемую умножением, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.

$U = \сум ^ {N-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="unitarygenerator--intint---t--unit--is-adj--ctl"></a>Унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  "года + CTL")

Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.


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

- [*Эндрю M. дочерние, Дмитрий Маслов, Вьетнам юнсеонг, Нил J. Росс (, Юань SU*, арксив: 1711.10980](https://arxiv.org/abs/1711.10980)