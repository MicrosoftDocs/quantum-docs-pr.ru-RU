---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 3f698a00b2c8d94b7cb3cca4f1721c659918f4a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732697"
---
# <a name="modulusi-function"></a>Функция Модулуси

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Вычисление канонического ресидуе `value` остатка от деления `modulus` .

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Значение, для которого вычислено ресидуе


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Модуль, по которому ресидуес принимаются, должен быть положительным



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю

## <a name="remarks"></a>Remarks

Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.