---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847292"
---
# <a name="modulusi-function"></a>Функция Модулуси

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является неотрицательным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.