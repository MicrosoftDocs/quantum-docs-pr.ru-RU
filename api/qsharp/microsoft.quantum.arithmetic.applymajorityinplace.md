---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Операция Апплимажоритинплаце
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: c32d7546fb753f78a72479cec11a6ed09c5e6179
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190740"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="08e20-102">Операция Апплимажоритинплаце</span><span class="sxs-lookup"><span data-stu-id="08e20-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="08e20-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="08e20-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="08e20-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08e20-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08e20-105">Применяет кубитную операцию "большинство" на месте к регистру Кубитс.</span><span class="sxs-lookup"><span data-stu-id="08e20-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="08e20-106">Описание</span><span class="sxs-lookup"><span data-stu-id="08e20-106">Description</span></span>

<span data-ttu-id="08e20-107">Эта операция выполняет вычисление функции большинства на месте 3 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="08e20-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="08e20-108">Если мы обкубити выходные данные как $z $ и input Кубитс как $x $ и $y $, операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \Кет{\операторнаме{МАЖ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="08e20-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="08e20-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="08e20-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="08e20-110">выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="08e20-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="08e20-111">Первая входная кубит.</span><span class="sxs-lookup"><span data-stu-id="08e20-111">First input qubit.</span></span> <span data-ttu-id="08e20-112">Обратите внимание, что выходные данные вычисляются на месте и хранятся в этом кубит.</span><span class="sxs-lookup"><span data-stu-id="08e20-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="08e20-113">входные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="08e20-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="08e20-114">Второй и третий входные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="08e20-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="08e20-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08e20-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

