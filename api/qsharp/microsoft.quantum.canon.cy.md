---
uid: Microsoft.Quantum.Canon.CY
title: Операция CY
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4a1a533421dd9205e973d5e8237d67b20bc4886d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216580"
---
# <a name="cy-operation"></a><span data-ttu-id="4a34d-102">Операция CY</span><span class="sxs-lookup"><span data-stu-id="4a34d-102">CY operation</span></span>

<span data-ttu-id="4a34d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4a34d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4a34d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a34d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a34d-105">Применяет шлюз с управляемой Y (CY) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="4a34d-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="4a34d-106">$ $ \бегин{алигн} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & я & 0 \енд{алигн}, $ $, где строки и столбцы упорядочены в соответствии с руководством по работе с тактовыми концепциями.</span><span class="sxs-lookup"><span data-stu-id="4a34d-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4a34d-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4a34d-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="4a34d-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4a34d-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4a34d-109">Управление кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="4a34d-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="4a34d-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4a34d-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4a34d-111">Целевой кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="4a34d-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4a34d-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a34d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a34d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a34d-113">Remarks</span></span>

<span data-ttu-id="4a34d-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="4a34d-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```