---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Определяемый пользователем тип Фаселиттлиндиан
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843005"
---
# <a name="phaselittleendian-user-defined-type"></a>Определяемый пользователем тип Фаселиттлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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