---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Операция Аппликсоринплаце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 8f338d6638d554f3ead1f3c0e7b6605c7937abd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843470"
---
# <a name="applyxorinplace-operation"></a><span data-ttu-id="27daf-102">Операция Аппликсоринплаце</span><span class="sxs-lookup"><span data-stu-id="27daf-102">ApplyXorInPlace operation</span></span>

<span data-ttu-id="27daf-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="27daf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="27daf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="27daf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="27daf-105">Применяет операцию побитового исключающего XOR между классическим целым числом и целым числом, представленным регистром Кубитс.</span><span class="sxs-lookup"><span data-stu-id="27daf-105">Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.</span></span>

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="27daf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="27daf-106">Description</span></span>

<span data-ttu-id="27daf-107">Применяет `X` операции к Кубитс в регистре с прямым порядком следования на основе 1 битов в целом.</span><span class="sxs-lookup"><span data-stu-id="27daf-107">Applies `X` operations to qubits in a little-endian register based on 1 bits in an integer.</span></span>

<span data-ttu-id="27daf-108">Давайте обстоится в `value` , а y — это целое число без знака, закодированное в `target` , а затем `InPlaceXorLE` выполняет операцию, указанную в следующем сопоставлении: $ \кет{и}\ригхтарров \кет{и\оплус a} $, где $ \оплус $ является побитовым ИСКЛЮЧАЮЩИМ оператором или.</span><span class="sxs-lookup"><span data-stu-id="27daf-108">Let us denote `value` by a and let y be an unsigned integer encoded in `target`, then `InPlaceXorLE` performs an operation given by the following map: $\ket{y}\rightarrow \ket{y\oplus a}$ , where $\oplus$ is the bitwise exclusive OR operator.</span></span>

## <a name="input"></a><span data-ttu-id="27daf-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="27daf-109">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="27daf-110">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="27daf-110">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="27daf-111">Целочисленное значение, которое считается неотрицательным.</span><span class="sxs-lookup"><span data-stu-id="27daf-111">An integer which is assumed to be non-negative.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="27daf-112">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="27daf-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="27daf-113">Регистр такта, который используется для хранения `value` в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="27daf-113">A quantum register which is used to store `value` in little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="27daf-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27daf-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

