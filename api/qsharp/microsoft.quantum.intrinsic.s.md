---
uid: Microsoft.Quantum.Intrinsic.S
title: Операция S
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: 8a57c60ac1df8f6e94b58acf7183c47f395d291a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732448"
---
# <a name="s-operation"></a><span data-ttu-id="f1004-102">Операция S</span><span class="sxs-lookup"><span data-stu-id="f1004-102">S operation</span></span>

<span data-ttu-id="f1004-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="f1004-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="f1004-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f1004-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f1004-105">Применяет шлюз S к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="f1004-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="f1004-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f1004-106">Description</span></span>

<span data-ttu-id="f1004-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} S \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & i \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="f1004-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="f1004-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="f1004-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="f1004-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f1004-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="f1004-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f1004-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f1004-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="f1004-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f1004-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f1004-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

