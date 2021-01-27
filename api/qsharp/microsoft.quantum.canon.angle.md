---
uid: Microsoft.Quantum.Canon.Angle
title: Angle, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 0528f21b2d9c98b6497e28741964e6497d4d0fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842037"
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

