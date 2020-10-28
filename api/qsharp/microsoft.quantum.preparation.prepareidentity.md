---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Операция Препареидентити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: a3f96fbdafb19c90fb2b563243600cca60841566
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733728"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="53552-102">Операция Препареидентити</span><span class="sxs-lookup"><span data-stu-id="53552-102">PrepareIdentity operation</span></span>

<span data-ttu-id="53552-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="53552-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="53552-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="53552-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="53552-105">При наличии регистра подготавливает эту регистрацию в максимальном смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="53552-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="53552-106">Регистрация подготавливается в состоянии $ \болдоне/2 ^ N $, применяя полный канал деполаризинг к каждому кубит, где $N $ — это длина регистра.</span><span class="sxs-lookup"><span data-stu-id="53552-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="53552-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="53552-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="53552-108">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53552-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="53552-109">Регистр, состояние которого необходимо деполяровать, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="53552-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="53552-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="53552-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="53552-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="53552-111">See Also</span></span>

- [<span data-ttu-id="53552-112">Microsoft. тактов. подготовка. Препаресинглекубитидентити</span><span class="sxs-lookup"><span data-stu-id="53552-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)