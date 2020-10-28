---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731689"
---
# <a name="assertmostsignificantbit-operation"></a>Операция Ассертмостсигнификантбит

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Утверждает, что наиболее значимые кубит регистра кубит, представляющие целое число без знака, находятся в определенном состоянии.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="value--__invalidresult__"></a>значение: __недопустимо <Result>__

Значение самого высокого бита, для которого выполняется утверждение.


### <a name="number--littleendian"></a>число: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Целое число без знака, для которого установлен наибольший бит.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Контролируемая версия этой операции не учитывает элементы управления.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. внутренний. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)