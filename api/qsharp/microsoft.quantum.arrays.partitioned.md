---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220507"
---
# <a name="partitioned-function"></a>Секционированная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Разделяет массив на несколько частей.

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Входные данные

### <a name="nelements--int"></a>Нелементс: [int](xref:microsoft.quantum.lang-ref.int)[]

Число элементов в каждой части массива


### <a name="arr--t"></a>ARR: 'T []

Входной массив для разбиения.



## <a name="output--t"></a>Выходные данные: 'T [] []

Несколько массивов, в которых первый массив является первым, `nElements[0]` `arr` а второй массив — рядом и `nElements[1]` `arr` т. д. Последний массив будет содержать все оставшиеся элементы.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

