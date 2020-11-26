---
uid: Microsoft.Quantum.Canon.Angle
title: Angle, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 1d8a9c2c19469e4949f043edd1ba91021fa42e78
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219419"
---
# <a name="angle-function"></a>Angle, функция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение 1, если `index` имеет нечетное число 1 и-1, если `index` имеет четное число 1.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>Описание

Значение соответствует знаку коэффициента Rademacher-Walsh спектра из n-переменных и функции для заданного присваивания, которое определяет угол поворота.

## <a name="input"></a>Входные данные

### <a name="index--int"></a>Индекс: [int](xref:microsoft.quantum.lang-ref.int)

Присваивание входных данных в виде целого числа (от 0 до 2 ^ n-1)



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

