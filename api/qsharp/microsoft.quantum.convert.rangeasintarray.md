---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Функция Ранжеасинтаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713367"
---
# <a name="rangeasintarray-function"></a>Функция Ранжеасинтаррай

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


Создает массив `arr` целых чисел, перечисленных с помощью Start.. шаг.. конце.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)

Объект `Range` из значений, `start..step..end` преобразуемых в массив.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Новый массив целых чисел, соответствующий значениям, перебираемым по `range` .