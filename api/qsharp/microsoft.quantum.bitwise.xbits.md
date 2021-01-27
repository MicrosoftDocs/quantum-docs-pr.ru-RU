---
uid: Microsoft.Quantum.Bitwise.XBits
title: Функция Ксбитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845245"
---
# <a name="xbits-function"></a>Функция Ксбитс

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает целое число, представляющее X бит массива операторов Паули.

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив операторов Паули, которые должны быть представлены в виде целого числа.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленное $x $ с двоичным представлением $ (p_ {62} \, p_ {61} \, \дотс \, p_0) $, где $p _i = $0, если `paulis[i]` имеет значение `PauliI` или `PauliZ` и, где $p _i = $1, если `paulis[i]` имеет значение `PauliX` или `PauliY` .

## <a name="remarks"></a>Remarks

Функция вызывает исключение, если длина `paulis` массива больше 63.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. побитовое. Збитс](xref:Microsoft.Quantum.Bitwise.ZBits)