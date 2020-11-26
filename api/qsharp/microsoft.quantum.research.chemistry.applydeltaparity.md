---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Операция Апплиделтапарити
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: 40157b6a166b09c6fee63d86e203f92069d008f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225760"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="eb141-102">Операция Апплиделтапарити</span><span class="sxs-lookup"><span data-stu-id="eb141-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="eb141-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="eb141-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="eb141-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="eb141-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="eb141-105">Вычисление разницы между предыдущим ПКРС... условия и следующие ПКРС... термин.</span><span class="sxs-lookup"><span data-stu-id="eb141-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="eb141-106">Это различие вычислено на вспомогательной кубит.</span><span class="sxs-lookup"><span data-stu-id="eb141-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="eb141-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eb141-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="eb141-108">Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="eb141-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="eb141-109">Список индексов для предыдущего ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="eb141-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="eb141-110">Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="eb141-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="eb141-111">Список индексов для следующего ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="eb141-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="eb141-112">AUX: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="eb141-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="eb141-113">Вспомогательная кубит, на которой сохраняются результаты вычисления четности.</span><span class="sxs-lookup"><span data-stu-id="eb141-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="eb141-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eb141-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eb141-115">Кубит, обрабатываемый всеми ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="eb141-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb141-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb141-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="eb141-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb141-117">Remarks</span></span>

<span data-ttu-id="eb141-118">Предполагается, что индексы P < Q < R < S <... для Превпк и Некстпк.</span><span class="sxs-lookup"><span data-stu-id="eb141-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>