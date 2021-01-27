---
uid: Microsoft.Quantum.Intrinsic.H
title: Операция H
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: H
qsharp.summary: >-
  Applies the Hadamard transformation to a single qubit.

  \begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}. \end{align}
ms.openlocfilehash: 6fa712b00a2745d8c0d8d3198cc9c5e6af3e2400
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818989"
---
# <a name="h-operation"></a><span data-ttu-id="1816a-102">Операция H</span><span class="sxs-lookup"><span data-stu-id="1816a-102">H operation</span></span>

<span data-ttu-id="1816a-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="1816a-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="1816a-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1816a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1816a-105">Применяет преобразование Хадамард к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="1816a-105">Applies the Hadamard transformation to a single qubit.</span></span>

<span data-ttu-id="1816a-106">\бегин{алигн} H \масрел{: =} \фрак {1} {\скрт {2} } \бегин{бматрикс} 1 & 1 \\ \\ 1 &-1 \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="1816a-106">\begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="1816a-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="1816a-107">\end{align}</span></span>

```qsharp
operation H (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1816a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1816a-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="1816a-109">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1816a-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1816a-110">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="1816a-110">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1816a-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1816a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

