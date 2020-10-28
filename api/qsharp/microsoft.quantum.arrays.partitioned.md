---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730088"
---
# <a name="partitioned-function"></a>Секционированная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

