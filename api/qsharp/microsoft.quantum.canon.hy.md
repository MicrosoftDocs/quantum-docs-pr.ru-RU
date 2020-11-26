---
uid: Microsoft.Quantum.Canon.HY
title: Операция Хи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: HY
qsharp.summary: >-
  Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.

  The Y Hadamard transformation $H_Y = S H$ on a single qubit is:

  \begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}. \end{align}
ms.openlocfilehash: ceca8eab8cb8f16333cd7a1e3c24e6cebe4ec8d7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206839"
---
# <a name="hy-operation"></a><span data-ttu-id="89d67-102">Операция Хи</span><span class="sxs-lookup"><span data-stu-id="89d67-102">HY operation</span></span>

<span data-ttu-id="89d67-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="89d67-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="89d67-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="89d67-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="89d67-105">Применяет аналог по оси Y к преобразованию Хадамард, которое изменяет оси Z и Y.</span><span class="sxs-lookup"><span data-stu-id="89d67-105">Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.</span></span>

<span data-ttu-id="89d67-106">Преобразование Y Хадамард $H _Y = S H $ в одном кубит:</span><span class="sxs-lookup"><span data-stu-id="89d67-106">The Y Hadamard transformation $H_Y = S H$ on a single qubit is:</span></span>

<span data-ttu-id="89d67-107">\бегин{алигн} H_Y \масрел{: =} \фрак {1} {\скрт {2} } \бегин{бматрикс} 1 & 1 \\ \\ i &-i \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="89d67-107">\begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}.</span></span>
<span data-ttu-id="89d67-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="89d67-108">\end{align}</span></span>

```qsharp
operation HY (target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="89d67-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="89d67-109">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="89d67-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="89d67-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="89d67-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="89d67-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="89d67-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89d67-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="89d67-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="89d67-113">See Also</span></span>

- [<span data-ttu-id="89d67-114">Microsoft. тактов. внутренний. H</span><span class="sxs-lookup"><span data-stu-id="89d67-114">Microsoft.Quantum.Intrinsic.H</span></span>](xref:Microsoft.Quantum.Intrinsic.H)