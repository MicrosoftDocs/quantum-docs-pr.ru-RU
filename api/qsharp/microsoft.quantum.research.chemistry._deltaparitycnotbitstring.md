---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Функция _DeltaParityCNOTbitstring
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710848"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="5cefe-102">Функция _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="5cefe-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="5cefe-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5cefe-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="5cefe-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5cefe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5cefe-105">Классический этап обработки `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="5cefe-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="5cefe-106">При этом вычисляется список элементов управления Кубитс для оценки разницы четности между любыми двумя ПКРС... условия четной длины.</span><span class="sxs-lookup"><span data-stu-id="5cefe-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="5cefe-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5cefe-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="5cefe-108">Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5cefe-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="5cefe-109">Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5cefe-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="5cefe-110">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="5cefe-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="5cefe-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="5cefe-111">Remarks</span></span>

<span data-ttu-id="5cefe-112">Предполагается, что длина терминов равна.</span><span class="sxs-lookup"><span data-stu-id="5cefe-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="5cefe-113">Вычисление списка элементов управления для разницы четности между любыми двумя терминами.</span><span class="sxs-lookup"><span data-stu-id="5cefe-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="5cefe-114">Предполагается, что списки ввода сортируются в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="5cefe-114">This assumes that the input lists is sorted in ascending order.</span></span>