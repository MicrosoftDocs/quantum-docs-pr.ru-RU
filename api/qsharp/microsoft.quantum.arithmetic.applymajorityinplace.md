---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Операция Апплимажоритинплаце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731833"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="3d066-102">Операция Апплимажоритинплаце</span><span class="sxs-lookup"><span data-stu-id="3d066-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="3d066-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3d066-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3d066-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3d066-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3d066-105">Применяет кубитную операцию "большинство" на месте к регистру Кубитс.</span><span class="sxs-lookup"><span data-stu-id="3d066-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="3d066-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3d066-106">Description</span></span>

<span data-ttu-id="3d066-107">Эта операция выполняет вычисление функции большинства на месте 3 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="3d066-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="3d066-108">Если мы обкубити выходные данные как $z $ и input Кубитс как $x $ и $y $, операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \Кет{\операторнаме{МАЖ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="3d066-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="3d066-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d066-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="3d066-110">выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3d066-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3d066-111">Первая входная кубит.</span><span class="sxs-lookup"><span data-stu-id="3d066-111">First input qubit.</span></span> <span data-ttu-id="3d066-112">Обратите внимание, что выходные данные вычисляются на месте и хранятся в этом кубит.</span><span class="sxs-lookup"><span data-stu-id="3d066-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="3d066-113">входные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3d066-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3d066-114">Второй и третий входные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="3d066-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3d066-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d066-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

