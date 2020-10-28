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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="2f19b-102">Определяемый пользователем тип Фаселиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="2f19b-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="2f19b-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2f19b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2f19b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2f19b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2f19b-105">Целые числа без знака с прямым порядком байтов на основе Кфт.</span><span class="sxs-lookup"><span data-stu-id="2f19b-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="2f19b-106">Например, если $ \кет{КС} $ является обратно-байтовым кодированием целого числа $x $ в вычислительной базе, то $ \Операторнаме{кфтле} \кет{КС} $ является кодировкой $x $ в базе Кфт.</span><span class="sxs-lookup"><span data-stu-id="2f19b-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="2f19b-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="2f19b-107">Remarks</span></span>

<span data-ttu-id="2f19b-108">Мы предлагаем сокращение, `PhaseLittleEndian` как `PhaseLE` в документации.</span><span class="sxs-lookup"><span data-stu-id="2f19b-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f19b-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="2f19b-109">See Also</span></span>

- [<span data-ttu-id="2f19b-110">Microsoft. тактов. Canon. Кфт</span><span class="sxs-lookup"><span data-stu-id="2f19b-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="2f19b-111">Microsoft. тактов. Canon. КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="2f19b-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)