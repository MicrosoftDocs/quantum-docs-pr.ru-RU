---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Функция Ранжеасинтаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850107"
---
# <a name="rangeasintarray-function"></a>Функция Ранжеасинтаррай

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает массив `arr` целых чисел, перечисленных с помощью Start.. шаг.. конце.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)

Объект `Range` из значений, `start..step..end` преобразуемых в массив.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Новый массив целых чисел, соответствующий значениям, перебираемым по `range` .

## <a name="example"></a>Пример

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```