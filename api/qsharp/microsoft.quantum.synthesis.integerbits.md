---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Функция Интежербитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730665"
---
# <a name="integerbits-function"></a>Функция Интежербитс

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакеты [](https://nuget.org/packages/)


Возвращает все позиции, в которых заданы биты целого числа.

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Неотрицательное число.


### <a name="length--int"></a>Длина: [int](xref:microsoft.quantum.lang-ref.int)

Число битов в расширении двоичного объекта `value` .



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив, содержащий все позиции бита (начиная с 0), которые являются 1 в расширении двоичного файла, `value` учитывая все биты до позиции `length - 1` .  Все позиции упорядочиваются в массиве по позиции в порядке возрастания.