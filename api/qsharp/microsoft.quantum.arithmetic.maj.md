---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Операция Shift
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731448"
---
# <a name="maj-operation"></a><span data-ttu-id="064f5-102">Операция Shift</span><span class="sxs-lookup"><span data-stu-id="064f5-102">MAJ operation</span></span>

<span data-ttu-id="064f5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="064f5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="064f5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="064f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="064f5-105">Это применяет операцию большинства "на месте" к 3 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="064f5-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="064f5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="064f5-106">Description</span></span>

<span data-ttu-id="064f5-107">Если мы обкубит состояние целевого объекта как $ \кет{з} $, а входные состояния входных Кубитс как $ \кет{КС} $ и $ \кет{и} $, эта операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="064f5-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="064f5-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="064f5-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="064f5-109">input0: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="064f5-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="064f5-110">Первый входной кубит.</span><span class="sxs-lookup"><span data-stu-id="064f5-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="064f5-111">INPUT1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="064f5-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="064f5-112">Второй входной кубит.</span><span class="sxs-lookup"><span data-stu-id="064f5-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="064f5-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="064f5-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="064f5-114">Кубит, на который будет применена функция большинства.</span><span class="sxs-lookup"><span data-stu-id="064f5-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="064f5-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="064f5-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

