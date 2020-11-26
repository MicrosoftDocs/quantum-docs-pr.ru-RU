---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Функция Збитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219453"
---
# <a name="zbits-function"></a>Функция Збитс

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает целое число, представляющее Z бит массива операторов Паули.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив операторов Паули, которые должны быть представлены в виде целого числа.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленное $x $ с двоичным представлением $ (p_ {62} \, p_ {61} \, \дотс \, p_0) $, где $p _i = $0, если `paulis[i]` имеет значение `PauliI` или `PauliX` и, где $p _i = $1, если `paulis[i]` имеет значение `PauliY` или `PauliZ` .

## <a name="remarks"></a>Комментарии

Функция вызывает исключение, если длина `paulis` массива больше 63.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. побитовое. Ксбитс](xref:Microsoft.Quantum.Bitwise.XBits)