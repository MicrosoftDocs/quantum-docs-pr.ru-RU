---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Операция Shift
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846550"
---
# <a name="maj-operation"></a><span data-ttu-id="e2ef5-102">Операция Shift</span><span class="sxs-lookup"><span data-stu-id="e2ef5-102">MAJ operation</span></span>

<span data-ttu-id="e2ef5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e2ef5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e2ef5-105">Это применяет операцию большинства "на месте" к 3 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e2ef5-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e2ef5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e2ef5-106">Description</span></span>

<span data-ttu-id="e2ef5-107">Если мы обкубит состояние целевого объекта как $ \кет{з} $, а входные состояния входных Кубитс как $ \кет{КС} $ и $ \кет{и} $, эта операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="e2ef5-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="e2ef5-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e2ef5-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="e2ef5-109">input0: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e2ef5-110">Первый входной кубит.</span><span class="sxs-lookup"><span data-stu-id="e2ef5-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="e2ef5-111">INPUT1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e2ef5-112">Второй входной кубит.</span><span class="sxs-lookup"><span data-stu-id="e2ef5-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e2ef5-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e2ef5-114">Кубит, на который будет применена функция большинства.</span><span class="sxs-lookup"><span data-stu-id="e2ef5-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e2ef5-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e2ef5-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

