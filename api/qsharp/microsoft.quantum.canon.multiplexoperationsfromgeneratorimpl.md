---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGeneratorImpl
title: Операция Мултиплексоператионсфромженераторимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGeneratorImpl
qsharp.summary: Implementation step of `MultiplexOperationsFromGenerator`.
ms.openlocfilehash: 98ba9cd24f04b8417cb176ee1630402483bc3b52
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206057"
---
# <a name="multiplexoperationsfromgeneratorimpl-operation"></a>Операция Мултиплексоператионсфромженераторимпл

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Шаг реализации `MultiplexOperationsFromGenerator` .

```qsharp
operation MultiplexOperationsFromGeneratorImpl<'T> (unitaryGenerator : (Int, Int, (Int -> ('T => Unit is Adj + Ctl))), auxiliary : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="unitarygenerator--intintint---t--unit--is-adj--ctl"></a>Унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> t => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL")




### <a name="auxiliary--qubit"></a>вспомогательная: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="index--littleendian"></a>Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)




### <a name="target--t"></a>Целевой объект: 'T





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Мултиплексоператионсфромженератор](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)