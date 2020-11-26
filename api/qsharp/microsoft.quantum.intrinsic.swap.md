---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: Операция переключения
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: e93c976f2fdf02de77fafa4d22e95fe9a33a9ba6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198424"
---
# <a name="swap-operation"></a><span data-ttu-id="66e92-102">Операция переключения</span><span class="sxs-lookup"><span data-stu-id="66e92-102">SWAP operation</span></span>

<span data-ttu-id="66e92-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="66e92-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="66e92-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="66e92-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="66e92-105">Применяет шлюз подкачки к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="66e92-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="66e92-106">\бегин{алигн} \Операторнаме{СВАП} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \енд{бматрикс}, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="66e92-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="66e92-107">где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="66e92-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="66e92-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66e92-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="66e92-109">qubit1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="66e92-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="66e92-110">Первый кубит, который нужно поменять местами.</span><span class="sxs-lookup"><span data-stu-id="66e92-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="66e92-111">qubit2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="66e92-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="66e92-112">Второй кубит, который необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="66e92-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="66e92-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66e92-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="66e92-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66e92-114">Remarks</span></span>

<span data-ttu-id="66e92-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="66e92-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```