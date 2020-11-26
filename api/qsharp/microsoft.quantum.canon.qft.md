---
uid: Microsoft.Quantum.Canon.QFT
title: Операция Кфт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 8f1aa8c3680a068e500503ca25afa9a49e4ef5bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205546"
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



## <a name="remarks"></a>Комментарии

Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)