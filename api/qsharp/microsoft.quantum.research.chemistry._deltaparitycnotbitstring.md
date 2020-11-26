---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Функция _DeltaParityCNOTbitstring
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226083"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="17b5b-102">Функция _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="17b5b-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="17b5b-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="17b5b-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="17b5b-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="17b5b-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="17b5b-105">Классический этап обработки `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="17b5b-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="17b5b-106">При этом вычисляется список элементов управления Кубитс для оценки разницы четности между любыми двумя ПКРС... условия четной длины.</span><span class="sxs-lookup"><span data-stu-id="17b5b-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="17b5b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="17b5b-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="17b5b-108">Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="17b5b-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="17b5b-109">Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="17b5b-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="17b5b-110">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="17b5b-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="17b5b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17b5b-111">Remarks</span></span>

<span data-ttu-id="17b5b-112">Предполагается, что длина терминов равна.</span><span class="sxs-lookup"><span data-stu-id="17b5b-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="17b5b-113">Вычисление списка элементов управления для разницы четности между любыми двумя терминами.</span><span class="sxs-lookup"><span data-stu-id="17b5b-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="17b5b-114">Предполагается, что списки ввода сортируются в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="17b5b-114">This assumes that the input lists is sorted in ascending order.</span></span>