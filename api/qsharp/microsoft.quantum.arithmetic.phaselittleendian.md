---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Определяемый пользователем тип Фаселиттлиндиан
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: f1f792d62004a2765d4e63870f5a41a4377b0d34
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730592"
---
# <a name="phaselittleendian-user-defined-type"></a>Определяемый пользователем тип Фаселиттлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Целые числа без знака с прямым порядком байтов на основе Кфт.

Например, если $ \кет{КС} $ является обратно-байтовым кодированием целого числа $x $ в вычислительной базе, то $ \Операторнаме{кфтле} \кет{КС} $ является кодировкой $x $ в базе Кфт.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Remarks

Мы предлагаем сокращение, `PhaseLittleEndian` как `PhaseLE` в документации.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кфт](xref:Microsoft.Quantum.Canon.QFT)
- [Microsoft. тактов. Canon. КФТЛЕ](xref:Microsoft.Quantum.Canon.QFTLE)