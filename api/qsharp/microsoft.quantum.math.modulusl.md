---
uid: Microsoft.Quantum.Math.ModulusL
title: Функция модуля
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842750"
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

## <a name="remarks"></a>Remarks

Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является неотрицательным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.