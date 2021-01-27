---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Операция Препареидентити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: ec7e813110ccd9e6d499fc469fa27249a182b870
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855874"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="d4a95-102">Операция Препареидентити</span><span class="sxs-lookup"><span data-stu-id="d4a95-102">PrepareIdentity operation</span></span>

<span data-ttu-id="d4a95-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d4a95-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d4a95-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4a95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4a95-105">При наличии регистра подготавливает эту регистрацию в максимальном смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d4a95-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="d4a95-106">Регистрация подготавливается в состоянии $ \болдоне/2 ^ N $, применяя полный канал деполаризинг к каждому кубит, где $N $ — это длина регистра.</span><span class="sxs-lookup"><span data-stu-id="d4a95-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d4a95-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d4a95-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="d4a95-108">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4a95-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d4a95-109">Регистр, состояние которого необходимо деполяровать, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="d4a95-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4a95-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4a95-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d4a95-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="d4a95-111">See Also</span></span>

- [<span data-ttu-id="d4a95-112">Microsoft. тактов. подготовка. Препаресинглекубитидентити</span><span class="sxs-lookup"><span data-stu-id="d4a95-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)