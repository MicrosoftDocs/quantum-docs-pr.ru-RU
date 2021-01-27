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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="57b2c-102">Определяемый пользователем тип Фаселиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="57b2c-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="57b2c-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="57b2c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="57b2c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="57b2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="57b2c-105">Целые числа без знака с прямым порядком байтов на основе Кфт.</span><span class="sxs-lookup"><span data-stu-id="57b2c-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="57b2c-106">Например, если $ \кет{КС} $ является обратно-байтовым кодированием целого числа $x $ в вычислительной базе, то $ \Операторнаме{кфтле} \кет{КС} $ является кодировкой $x $ в базе Кфт.</span><span class="sxs-lookup"><span data-stu-id="57b2c-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="57b2c-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="57b2c-107">Remarks</span></span>

<span data-ttu-id="57b2c-108">Мы предлагаем сокращение, `PhaseLittleEndian` как `PhaseLE` в документации.</span><span class="sxs-lookup"><span data-stu-id="57b2c-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="57b2c-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="57b2c-109">See Also</span></span>

- [<span data-ttu-id="57b2c-110">Microsoft. тактов. Canon. Кфт</span><span class="sxs-lookup"><span data-stu-id="57b2c-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="57b2c-111">Microsoft. тактов. Canon. КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="57b2c-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)