---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Операция кнот
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 02ae795c785dcbc25b56ac513a9237540e57ea63
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849438"
---
# <a name="cnot-operation"></a><span data-ttu-id="9fddc-102">Операция кнот</span><span class="sxs-lookup"><span data-stu-id="9fddc-102">CNOT operation</span></span>

<span data-ttu-id="9fddc-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9fddc-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9fddc-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9fddc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9fddc-105">Применяет шлюз управляемого объекта (кнот) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="9fddc-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="9fddc-106">\бегин{алигн} \Операторнаме{кнот} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{бматрикс}, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="9fddc-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="9fddc-107">где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="9fddc-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9fddc-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9fddc-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="9fddc-109">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9fddc-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9fddc-110">Управление кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="9fddc-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9fddc-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9fddc-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9fddc-112">Целевой кубит для шлюза кнот.</span><span class="sxs-lookup"><span data-stu-id="9fddc-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9fddc-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9fddc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9fddc-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="9fddc-114">Remarks</span></span>

<span data-ttu-id="9fddc-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="9fddc-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```