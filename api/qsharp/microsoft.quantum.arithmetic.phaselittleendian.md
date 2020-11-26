---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Определяемый пользователем тип Фаселиттлиндиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 45b824a74d664df0d5707264a3c616fb27c477b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222428"
---
# <a name="phaselittleendian-user-defined-type"></a>Определяемый пользователем тип Фаселиттлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Целые числа без знака с прямым порядком байтов на основе Кфт.

Например, если $ \кет{КС} $ является обратно-байтовым кодированием целого числа $x $ в вычислительной базе, то $ \Операторнаме{кфтле} \кет{КС} $ является кодировкой $x $ в базе Кфт.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Комментарии

Мы предлагаем сокращение, `PhaseLittleEndian` как `PhaseLE` в документации.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кфт](xref:Microsoft.Quantum.Canon.QFT)
- [Microsoft. тактов. Canon. КФТЛЕ](xref:Microsoft.Quantum.Canon.QFTLE)