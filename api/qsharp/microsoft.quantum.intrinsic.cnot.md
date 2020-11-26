---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Операция кнот
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 90e84f7d0ea7373498632474dfafa23335f0c78e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198982"
---
# <a name="cnot-operation"></a><span data-ttu-id="9ffaa-102">Операция кнот</span><span class="sxs-lookup"><span data-stu-id="9ffaa-102">CNOT operation</span></span>

<span data-ttu-id="9ffaa-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9ffaa-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9ffaa-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9ffaa-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9ffaa-105">Применяет шлюз управляемого объекта (кнот) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="9ffaa-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="9ffaa-106">\бегин{алигн} \Операторнаме{кнот} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{бматрикс}, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="9ffaa-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="9ffaa-107">где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="9ffaa-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9ffaa-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ffaa-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="9ffaa-109">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ffaa-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ffaa-110">Управление кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="9ffaa-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9ffaa-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ffaa-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ffaa-112">Целевой кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="9ffaa-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ffaa-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ffaa-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9ffaa-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ffaa-114">Remarks</span></span>

<span data-ttu-id="9ffaa-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="9ffaa-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```