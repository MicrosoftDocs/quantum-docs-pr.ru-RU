---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Функция _DeltaParityCNOTbitstring
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847604"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="654da-102">Функция _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="654da-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="654da-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="654da-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="654da-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="654da-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="654da-105">Классический этап обработки `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="654da-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="654da-106">При этом вычисляется список элементов управления Кубитс для оценки разницы четности между любыми двумя ПКРС... условия четной длины.</span><span class="sxs-lookup"><span data-stu-id="654da-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="654da-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="654da-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="654da-108">Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="654da-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="654da-109">Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="654da-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="654da-110">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="654da-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="654da-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="654da-111">Remarks</span></span>

<span data-ttu-id="654da-112">Предполагается, что длина терминов равна.</span><span class="sxs-lookup"><span data-stu-id="654da-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="654da-113">Вычисление списка элементов управления для разницы четности между любыми двумя терминами.</span><span class="sxs-lookup"><span data-stu-id="654da-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="654da-114">Предполагается, что списки ввода сортируются в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="654da-114">This assumes that the input lists is sorted in ascending order.</span></span>