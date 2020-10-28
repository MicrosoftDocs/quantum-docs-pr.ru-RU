---
uid: Microsoft.Quantum.Bitwise.XBits
title: Функция Ксбитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 91619803c7efe56e617b16637f5302aa0b7978ec
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729809"
---
# <a name="xbits-function"></a>Функция Ксбитс

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакеты [](https://nuget.org/packages/)


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