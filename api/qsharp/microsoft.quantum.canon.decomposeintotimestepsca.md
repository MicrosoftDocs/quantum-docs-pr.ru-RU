---
uid: Microsoft.Quantum.Canon.DecomposeIntoTimeStepsCA
title: Функция Декомпосеинтотиместепска
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposeIntoTimeStepsCA
qsharp.summary: >-
  > [!WARNING]

  > DecomposeIntoTimeStepsCA has been deprecated. Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.
ms.openlocfilehash: b6f3fe0ececc58d86b916841c513377fbcb59054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716335"
---
# <a name="decomposeintotimestepsca-function"></a><span data-ttu-id="5ded0-102">Функция Декомпосеинтотиместепска</span><span class="sxs-lookup"><span data-stu-id="5ded0-102">DecomposeIntoTimeStepsCA function</span></span>

<span data-ttu-id="5ded0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5ded0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5ded0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5ded0-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="5ded0-105">Декомпосеинтотиместепска является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="5ded0-105">DecomposeIntoTimeStepsCA has been deprecated.</span></span> <span data-ttu-id="5ded0-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA>.</span><span class="sxs-lookup"><span data-stu-id="5ded0-106">Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.</span></span>



```qsharp
function DecomposeIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="5ded0-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5ded0-107">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="5ded0-108">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5ded0-108">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="5ded0-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="5ded0-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="trotterorder--int"></a><span data-ttu-id="5ded0-110">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5ded0-110">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--doublet--unit-adj--ctl"></a><span data-ttu-id="5ded0-111">Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [единицы](xref:microsoft.quantum.lang-ref.unit) и список доверия</span><span class="sxs-lookup"><span data-stu-id="5ded0-111">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5ded0-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5ded0-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5ded0-113">Е</span><span class="sxs-lookup"><span data-stu-id="5ded0-113">'T</span></span>

