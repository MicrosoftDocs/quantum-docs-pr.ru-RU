---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845543"
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



## <a name="example"></a>Пример

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```