---
uid: Microsoft.Quantum.Intrinsic.H
title: Операция H
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: H
qsharp.summary: >-
  Applies the Hadamard transformation to a single qubit.

  \begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}. \end{align}
ms.openlocfilehash: 6f02390588c9de38f69802575429aff749f70ac5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212381"
---
# <a name="h-operation"></a><span data-ttu-id="a9dea-102">Операция H</span><span class="sxs-lookup"><span data-stu-id="a9dea-102">H operation</span></span>

<span data-ttu-id="a9dea-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a9dea-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a9dea-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a9dea-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a9dea-105">Применяет преобразование Хадамард к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="a9dea-105">Applies the Hadamard transformation to a single qubit.</span></span>

<span data-ttu-id="a9dea-106">\бегин{алигн} H \масрел{: =} \фрак {1} {\скрт {2} } \бегин{бматрикс} 1 & 1 \\ \\ 1 &-1 \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="a9dea-106">\begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="a9dea-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="a9dea-107">\end{align}</span></span>

```qsharp
operation H (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a9dea-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a9dea-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="a9dea-109">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a9dea-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a9dea-110">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="a9dea-110">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a9dea-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a9dea-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

