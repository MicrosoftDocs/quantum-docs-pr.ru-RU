---
uid: Microsoft.Quantum.Canon.QFT
title: Операция Кфт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852294"
---
# <a name="qft-operation"></a>Операция Кфт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="qs--bigendian"></a>QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр такта, к которому применяется преобразование Фурье в тактовой области



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)