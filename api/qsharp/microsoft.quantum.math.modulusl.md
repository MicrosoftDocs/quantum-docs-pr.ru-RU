---
uid: Microsoft.Quantum.Math.ModulusL
title: Функция модуля
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 5c9a8ceceac5d2cdac6b82f7f74a85e9443382a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194939"
---
# <a name="modulusl-function"></a>Функция модуля

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление канонического ресидуе `value` остатка от деления `modulus` .

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>Входные данные

### <a name="value--bigint"></a>значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Значение, для которого вычислено ресидуе


### <a name="modulus--bigint"></a>модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Модуль, по которому ресидуес принимаются, должен быть положительным



## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю

## <a name="remarks"></a>Комментарии

Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.