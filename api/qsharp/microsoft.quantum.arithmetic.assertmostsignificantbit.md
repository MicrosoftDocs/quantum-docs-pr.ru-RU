---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843421"
---
# <a name="assertmostsignificantbit-operation"></a>Операция Ассертмостсигнификантбит

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Утверждает, что наиболее значимые кубит регистра кубит, представляющие целое число без знака, находятся в определенном состоянии.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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