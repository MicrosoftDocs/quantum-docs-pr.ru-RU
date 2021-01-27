---
uid: Microsoft.Quantum.Canon.CX
title: Операция CX
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: e27b30a6b4609daaac2cc5eda68120115777af0c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840753"
---
# <a name="cx-operation"></a><span data-ttu-id="85f5b-102">Операция CX</span><span class="sxs-lookup"><span data-stu-id="85f5b-102">CX operation</span></span>

<span data-ttu-id="85f5b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="85f5b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="85f5b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85f5b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85f5b-105">Применяет шлюз с управляемой X (CX) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="85f5b-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="85f5b-106">$ $ \бегин{алигн} \лефт (\бегин{Матрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{Матрикс}\ригхт) \енд{алигн}, $ $, где строки и столбцы упорядочены как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="85f5b-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="85f5b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="85f5b-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="85f5b-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="85f5b-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="85f5b-109">Управление кубит для шлюза CX.</span><span class="sxs-lookup"><span data-stu-id="85f5b-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="85f5b-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="85f5b-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="85f5b-111">Целевой кубит для шлюза CX.</span><span class="sxs-lookup"><span data-stu-id="85f5b-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85f5b-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85f5b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="85f5b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="85f5b-113">Remarks</span></span>

<span data-ttu-id="85f5b-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="85f5b-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="85f5b-115">и в:</span><span class="sxs-lookup"><span data-stu-id="85f5b-115">and to:</span></span>

```qsharp
CNOT(control, target);
```