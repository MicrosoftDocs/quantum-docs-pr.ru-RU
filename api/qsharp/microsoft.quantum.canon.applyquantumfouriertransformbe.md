---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Операция Аппликуантумфауриертрансформбе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: d15310298dc138bdffb612895bbf20ca1371db6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717791"
---
# <a name="applyquantumfouriertransformbe-operation"></a>Операция Аппликуантумфауриертрансформбе

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="qs--bigendian"></a>QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр такта, к которому применяется преобразование Фурье в тактовой области



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппроксиматекфт](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [Microsoft. тактов. Canon. КФТЛЕ](xref:Microsoft.Quantum.Canon.QFTLE)