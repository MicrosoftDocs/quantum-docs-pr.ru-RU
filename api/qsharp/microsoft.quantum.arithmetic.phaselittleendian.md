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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="16e28-102">Определяемый пользователем тип Фаселиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="16e28-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="16e28-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="16e28-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="16e28-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16e28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16e28-105">Целые числа без знака с прямым порядком байтов на основе Кфт.</span><span class="sxs-lookup"><span data-stu-id="16e28-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="16e28-106">Например, если $ \кет{КС} $ является обратно-байтовым кодированием целого числа $x $ в вычислительной базе, то $ \Операторнаме{кфтле} \кет{КС} $ является кодировкой $x $ в базе Кфт.</span><span class="sxs-lookup"><span data-stu-id="16e28-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="16e28-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e28-107">Remarks</span></span>

<span data-ttu-id="16e28-108">Мы предлагаем сокращение, `PhaseLittleEndian` как `PhaseLE` в документации.</span><span class="sxs-lookup"><span data-stu-id="16e28-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="16e28-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="16e28-109">See Also</span></span>

- [<span data-ttu-id="16e28-110">Microsoft. тактов. Canon. Кфт</span><span class="sxs-lookup"><span data-stu-id="16e28-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="16e28-111">Microsoft. тактов. Canon. КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="16e28-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)