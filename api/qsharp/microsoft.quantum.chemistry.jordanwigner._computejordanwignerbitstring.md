---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Функция _ComputeJordanWignerBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203949"
---
# <a name="_computejordanwignerbitstring-function"></a>Функция _ComputeJordanWignerBitString

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Вычисление Z-компонента Иордания — Вигнер строки между фермион индексами в операторе фермионик с четным числом операторов создания или аннихилатион.

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a>Входные данные

### <a name="nfermions--int"></a>Нфермионс: [int](xref:microsoft.quantum.lang-ref.int)

Число фермионс в системе.


### <a name="idxfermions--int"></a>Идксфермионс: [int](xref:microsoft.quantum.lang-ref.int)[]

Индексы операторов фермионик.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Битстринг `Bool[]` , `true` `PauliZ` к которому следует применить.