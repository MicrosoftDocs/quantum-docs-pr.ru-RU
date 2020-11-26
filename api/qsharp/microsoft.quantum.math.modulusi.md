---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6bbb3877b93e1fc6b38f85a716ba617311c7cfba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227783"
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

## <a name="remarks"></a>Комментарии

Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.