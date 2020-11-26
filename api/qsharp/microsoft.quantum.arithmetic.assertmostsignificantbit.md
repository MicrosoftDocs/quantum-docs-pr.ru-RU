---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223788"
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



## <a name="remarks"></a>Комментарии

Контролируемая версия этой операции не учитывает элементы управления.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. внутренний. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)