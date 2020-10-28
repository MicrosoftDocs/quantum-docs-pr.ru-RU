---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Операция кнот
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 2fb5b4df189fb3ab23b2ca5cb273b2451ffcc067
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732457"
---
# <a name="cnot-operation"></a><span data-ttu-id="27328-102">Операция кнот</span><span class="sxs-lookup"><span data-stu-id="27328-102">CNOT operation</span></span>

<span data-ttu-id="27328-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="27328-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="27328-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="27328-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="27328-105">Применяет шлюз управляемого объекта (кнот) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="27328-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="27328-106">\бегин{алигн} \Операторнаме{кнот} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{бматрикс}, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="27328-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="27328-107">где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="27328-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="27328-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="27328-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="27328-109">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="27328-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="27328-110">Управление кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="27328-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="27328-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="27328-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="27328-112">Целевой кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="27328-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="27328-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27328-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="27328-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="27328-114">Remarks</span></span>

<span data-ttu-id="27328-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="27328-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```