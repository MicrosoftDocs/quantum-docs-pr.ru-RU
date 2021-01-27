---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Операция Аппликуантумфауриертрансформ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: d99000c21c79d2ca97b1fe92ad331c7ba8599700
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844764"
---
# <a name="applyquantumfouriertransform-operation"></a>Операция Аппликуантумфауриертрансформ

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с прямым порядком байтов.

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="qs--littleendian"></a>QS: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта, к которому применяется преобразование Фурье в тактовой области



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что входные и выходные данные находятся в кодировке с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)