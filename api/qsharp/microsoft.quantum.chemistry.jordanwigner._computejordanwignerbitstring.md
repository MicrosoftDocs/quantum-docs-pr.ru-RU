---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Функция _ComputeJordanWignerBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839525"
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

## <a name="example"></a>Пример

Let Битстринг = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); Битстринг имеет значение [false, false, false, true, true, true, false].