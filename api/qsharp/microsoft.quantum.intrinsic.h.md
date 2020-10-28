---
uid: Microsoft.Quantum.Intrinsic.H
title: Операция H
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: H
qsharp.summary: >-
  Applies the Hadamard transformation to a single qubit.

  \begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}. \end{align}
ms.openlocfilehash: 1ba99d2f34c601b46b82fb853008464c3add965d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711464"
---
# <a name="h-operation"></a><span data-ttu-id="a200b-102">Операция H</span><span class="sxs-lookup"><span data-stu-id="a200b-102">H operation</span></span>

<span data-ttu-id="a200b-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a200b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a200b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a200b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a200b-105">Применяет преобразование Хадамард к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="a200b-105">Applies the Hadamard transformation to a single qubit.</span></span>

<span data-ttu-id="a200b-106">\бегин{алигн} H \масрел{: =} \фрак {1} {\скрт {2} } \бегин{бматрикс} 1 & 1 \\ \\ 1 &-1 \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="a200b-106">\begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="a200b-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="a200b-107">\end{align}</span></span>

```qsharp
operation H (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="a200b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a200b-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="a200b-109">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a200b-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a200b-110">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="a200b-110">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a200b-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a200b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

