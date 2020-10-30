---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Операция Аппликсоринплаце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 5a35abc16a967e64c84466a47844ed7beeb618dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731697"
---
# <a name="applyxorinplace-operation"></a><span data-ttu-id="20c5f-102">Операция Аппликсоринплаце</span><span class="sxs-lookup"><span data-stu-id="20c5f-102">ApplyXorInPlace operation</span></span>

<span data-ttu-id="20c5f-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="20c5f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="20c5f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20c5f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20c5f-105">Применяет операцию побитового исключающего XOR между классическим целым числом и целым числом, представленным регистром Кубитс.</span><span class="sxs-lookup"><span data-stu-id="20c5f-105">Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.</span></span>

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="20c5f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="20c5f-106">Description</span></span>

<span data-ttu-id="20c5f-107">Применяет `X` операции к Кубитс в регистре с прямым порядком следования на основе 1 битов в целом.</span><span class="sxs-lookup"><span data-stu-id="20c5f-107">Applies `X` operations to qubits in a little-endian register based on 1 bits in an integer.</span></span>

<span data-ttu-id="20c5f-108">Давайте обстоится в `value` , а y — это целое число без знака, закодированное в `target` , а затем `InPlaceXorLE` выполняет операцию, указанную в следующем сопоставлении: $ \кет{и}\ригхтарров \кет{и\оплус a} $, где $ \оплус $ является побитовым ИСКЛЮЧАЮЩИМ оператором или.</span><span class="sxs-lookup"><span data-stu-id="20c5f-108">Let us denote `value` by a and let y be an unsigned integer encoded in `target`, then `InPlaceXorLE` performs an operation given by the following map: $\ket{y}\rightarrow \ket{y\oplus a}$ , where $\oplus$ is the bitwise exclusive OR operator.</span></span>

## <a name="input"></a><span data-ttu-id="20c5f-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20c5f-109">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="20c5f-110">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="20c5f-110">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="20c5f-111">Целочисленное значение, которое считается неотрицательным.</span><span class="sxs-lookup"><span data-stu-id="20c5f-111">An integer which is assumed to be non-negative.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="20c5f-112">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="20c5f-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="20c5f-113">Регистр такта, который используется для хранения `value` в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="20c5f-113">A quantum register which is used to store `value` in little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="20c5f-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20c5f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
