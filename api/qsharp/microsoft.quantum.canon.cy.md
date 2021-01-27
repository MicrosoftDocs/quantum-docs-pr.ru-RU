---
uid: Microsoft.Quantum.Canon.CY
title: Операция CY
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 862f058e630ee6d9159e0fe514ca2dd1179ea9a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840738"
---
# <a name="cy-operation"></a><span data-ttu-id="037a2-102">Операция CY</span><span class="sxs-lookup"><span data-stu-id="037a2-102">CY operation</span></span>

<span data-ttu-id="037a2-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="037a2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="037a2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="037a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="037a2-105">Применяет шлюз с управляемой Y (CY) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="037a2-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="037a2-106">$ $ \бегин{алигн} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & я & 0 \енд{алигн}, $ $, где строки и столбцы упорядочены в соответствии с руководством по работе с тактовыми концепциями.</span><span class="sxs-lookup"><span data-stu-id="037a2-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="037a2-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="037a2-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="037a2-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="037a2-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="037a2-109">Управление кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="037a2-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="037a2-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="037a2-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="037a2-111">Целевой кубит для шлюза CY.</span><span class="sxs-lookup"><span data-stu-id="037a2-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="037a2-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="037a2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="037a2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="037a2-113">Remarks</span></span>

<span data-ttu-id="037a2-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="037a2-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```