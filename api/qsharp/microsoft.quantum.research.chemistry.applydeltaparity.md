---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Операция Апплиделтапарити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: f5f1d74274994f042f1bc3f2e0d5332f504be02c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851107"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="116c0-102">Операция Апплиделтапарити</span><span class="sxs-lookup"><span data-stu-id="116c0-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="116c0-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="116c0-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="116c0-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="116c0-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="116c0-105">Вычисление разницы между предыдущим ПКРС... условия и следующие ПКРС... термин.</span><span class="sxs-lookup"><span data-stu-id="116c0-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="116c0-106">Это различие вычислено на вспомогательной кубит.</span><span class="sxs-lookup"><span data-stu-id="116c0-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="116c0-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="116c0-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="116c0-108">Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="116c0-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="116c0-109">Список индексов для предыдущего ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="116c0-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="116c0-110">Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="116c0-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="116c0-111">Список индексов для следующего ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="116c0-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="116c0-112">AUX: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="116c0-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="116c0-113">Вспомогательная кубит, на которой сохраняются результаты вычисления четности.</span><span class="sxs-lookup"><span data-stu-id="116c0-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="116c0-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="116c0-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="116c0-115">Кубит, обрабатываемый всеми ПКРС... черт.</span><span class="sxs-lookup"><span data-stu-id="116c0-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="116c0-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="116c0-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="116c0-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="116c0-117">Remarks</span></span>

<span data-ttu-id="116c0-118">Предполагается, что индексы P < Q < R < S <... для Превпк и Некстпк.</span><span class="sxs-lookup"><span data-stu-id="116c0-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>