---
uid: Microsoft.Quantum.Canon.CY
title: Операция CY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 291891457ff39cf7092d17aa1d900dd0d35d9cf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716363"
---
# <a name="cy-operation"></a><span data-ttu-id="144a3-102">Операция CY</span><span class="sxs-lookup"><span data-stu-id="144a3-102">CY operation</span></span>

<span data-ttu-id="144a3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="144a3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="144a3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="144a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="144a3-105">Применяет шлюз с управляемой Y (CY) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="144a3-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="144a3-106">$ $ \бегин{алигн} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & я & 0 \енд{алигн}, $ $, где строки и столбцы упорядочены в соответствии с руководством по работе с тактовыми концепциями.</span><span class="sxs-lookup"><span data-stu-id="144a3-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="144a3-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="144a3-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="144a3-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="144a3-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="144a3-109">Управление кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="144a3-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="144a3-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="144a3-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="144a3-111">Целевой кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="144a3-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="144a3-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="144a3-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="144a3-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="144a3-113">Remarks</span></span>

<span data-ttu-id="144a3-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="144a3-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```