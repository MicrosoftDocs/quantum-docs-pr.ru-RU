---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Функция Интежербитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: d6566716f5a63c090668d9582b7b000c16d1f6a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231098"
---
# <a name="integerbits-function"></a>Функция Интежербитс

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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