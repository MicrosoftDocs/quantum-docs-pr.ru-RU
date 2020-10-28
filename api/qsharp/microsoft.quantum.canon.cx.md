---
uid: Microsoft.Quantum.Canon.CX
title: Операция CX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: c430525b71ad4ef0812d90a8ff20c41a5d5b8708
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716377"
---
# <a name="cx-operation"></a><span data-ttu-id="fee58-102">Операция CX</span><span class="sxs-lookup"><span data-stu-id="fee58-102">CX operation</span></span>

<span data-ttu-id="fee58-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fee58-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fee58-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fee58-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fee58-105">Применяет шлюз с управляемой X (CX) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="fee58-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="fee58-106">$ $ \бегин{алигн} \лефт (\бегин{Матрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{Матрикс}\ригхт) \енд{алигн}, $ $, где строки и столбцы упорядочены как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="fee58-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="fee58-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fee58-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="fee58-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fee58-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fee58-109">Управление кубит для шлюза CX.</span><span class="sxs-lookup"><span data-stu-id="fee58-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fee58-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fee58-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fee58-111">Целевой кубит для шлюза CX.</span><span class="sxs-lookup"><span data-stu-id="fee58-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fee58-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fee58-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fee58-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="fee58-113">Remarks</span></span>

<span data-ttu-id="fee58-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="fee58-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="fee58-115">и в:</span><span class="sxs-lookup"><span data-stu-id="fee58-115">and to:</span></span>

```qsharp
CNOT(control, target);
```