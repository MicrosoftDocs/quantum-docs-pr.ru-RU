---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Функция Збитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: d1ddc2a4cdbdfd3945885de856456b3108592594
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842064"
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

## <a name="remarks"></a>Remarks

Функция вызывает исключение, если длина `paulis` массива больше 63.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. побитовое. Ксбитс](xref:Microsoft.Quantum.Bitwise.XBits)