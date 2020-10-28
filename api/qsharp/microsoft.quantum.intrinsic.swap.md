---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: Операция переключения
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 18b910741e9d0883fc5fcd025eb647407c823269
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730768"
---
# <a name="swap-operation"></a><span data-ttu-id="133c5-102">Операция переключения</span><span class="sxs-lookup"><span data-stu-id="133c5-102">SWAP operation</span></span>

<span data-ttu-id="133c5-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="133c5-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="133c5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="133c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="133c5-105">Применяет шлюз подкачки к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="133c5-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="133c5-106">\бегин{алигн} \Операторнаме{СВАП} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \енд{бматрикс}, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="133c5-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="133c5-107">где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="133c5-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="133c5-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="133c5-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="133c5-109">qubit1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="133c5-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="133c5-110">Первый кубит, который нужно поменять местами.</span><span class="sxs-lookup"><span data-stu-id="133c5-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="133c5-111">qubit2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="133c5-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="133c5-112">Второй кубит, который необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="133c5-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="133c5-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="133c5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="133c5-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="133c5-114">Remarks</span></span>

<span data-ttu-id="133c5-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="133c5-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```