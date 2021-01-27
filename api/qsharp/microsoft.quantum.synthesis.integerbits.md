---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Функция Интежербитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855403"
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

## <a name="example"></a>Пример

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```